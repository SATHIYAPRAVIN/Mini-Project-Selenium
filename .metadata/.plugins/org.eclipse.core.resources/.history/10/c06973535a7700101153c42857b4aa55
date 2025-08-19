package com.main.utils;
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;
import java.io.FileInputStream;
import java.util.HashMap;
import java.util.Map;

public class ExcelUtils {
	public static Map<String, String> getInputsForKeyword(String keyword) {
	    Map<String, String> inputs = new HashMap<>();
	    try (FileInputStream fis = new FileInputStream("test-data/TestInputs.xlsx");
	         Workbook workbook = new XSSFWorkbook(fis)) {

	        Sheet sheet = workbook.getSheetAt(0);
	        for (Row row : sheet) {
	            if (row.getRowNum() == 0) continue;

	            String rowKeyword = row.getCell(1).getStringCellValue();
	            if (rowKeyword.equalsIgnoreCase(keyword)) {
	                String key = row.getCell(2).getStringCellValue();
                   String value = getCellValue(row.getCell(3));
	                inputs.put(key, value);
	            }
	        }
	    } catch (Exception e) {
	        e.printStackTrace();
	    }
	    return inputs;
	}
	private static String getCellValue(Cell cell) {
	    if (cell == null) return "";
	    switch (cell.getCellType()) {
	        case STRING:
	            return cell.getStringCellValue().trim();
	        case NUMERIC:
	            return String.valueOf((int) cell.getNumericCellValue()); // or use `cell.getNumericCellValue()` for decimals
	        case BOOLEAN:
	            return String.valueOf(cell.getBooleanCellValue());
	        case FORMULA:
	            return cell.getCellFormula();
	        default:
	            return "";
	    }
	}


}
