# 選藥系統（PySimpleGUI）

## 安裝

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -U pip
pip install -r requirements.txt
```

注意：此程式使用 PySimpleGUI（預設 tkinter）。在 Linux 上請確保系統已安裝 `python3-tk` 與圖形環境（`$DISPLAY`）。若在純命令列/無頭環境執行將無法顯示視窗。

## 執行

```bash
python medicine_gui.py
```

## 匯入資料
- 支援 TXT/CSV/TSV，會自動偵測分隔符。
- 若有標頭，會優先尋找包含「中文」「中文名稱」的欄位。
- 內容會去重並排序後顯示於清單。

## 匯出
- TXT：每行 `品名 x 數量`。
- CSV：包含欄位「藥品」「數量」，寫入編碼為 `UTF-8 with BOM` 以利 Excel 顯示中文。
