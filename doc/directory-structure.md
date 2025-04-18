# ディレクトリ構成案 - Inbase (iOS / SwiftUI)

```
Inbase/
├── InbaseApp.swift           # エントリーポイント
├── Assets.xcassets            # アセット管理（アイコン・色など）
├── Info.plist                 # アプリの設定ファイル
│
├── Models/                   # データモデル（Codable構造体）
│   ├── Invoice.swift
│   └── InvoiceItem.swift
│
├── Views/                    # 画面構成（SwiftUI）
│   ├── HomeView.swift
│   ├── ScanView.swift
│   ├── DetailView.swift
│   ├── EditView.swift
│   └── SettingsView.swift
│
├── ViewModels/               # ビジネスロジック・状態管理
│   ├── InvoiceViewModel.swift
│   └── ScanViewModel.swift
│
├── Services/                 # OCR・PDF処理・ファイル操作
│   ├── OCRService.swift
│   ├── PDFImportService.swift
│   └── FileStorageService.swift
│
├── Utils/                    # ユーティリティ関数・拡張
│   └── DateFormatter+Ext.swift
│
└── Resources/                # 定義ファイル・設定ファイル
    └── SampleData.json        # サンプルデータ（開発用）
```

## 備考
- SwiftUIアーキテクチャに則り、ViewとViewModelの責務を分離。
- Modelsは全てCodable対応。
- Services層でOCRや保存などのロジックを集約し、テスト・再利用を容易に。
- 小規模〜中規模アプリ向けのシンプルな構成。


