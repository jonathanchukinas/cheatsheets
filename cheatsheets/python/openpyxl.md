# openpyxl (Python module) Cheatsheet

Files & Sheets
- Import openpyxl
- wb = openpyxl.load_workbook("file_name.xlsx")
- Print(wb.sheetnames)
- Sheet = wb["Sheet1"]
- Wb.create_sheet("Sheet2", 0)
- Wb.remove_sheet(sheet)
- Sheet.max_row
- Sheet.max_column
- Sheet.append([1,2,3])
- Sheet.delete_rows/cols
- Wb.save("new_file_name.xlsx")

A1 Notation
- Cell = Sheet["a1"]
- Sheet["a"] - all cells in "a" column
- Sheet["a:c"]
- Sheet["a1:c3"]
- Sheet[1:3]
- Print(cell.value)
- Cell.value = 1
- Print(Cell.row)
- Print(cell.column)
- Print(cell.coordinate)

Cell Coordinates
- Cell = Sheet.cell(1,10) = "XYZ"
- Cell = Sheet.cell(row=1, column=1) = 345
	
Loop through cells
- For row in range(1, sheet.max_row+1):
	- do stuff
- Cell = sheet.cell(row, column)
