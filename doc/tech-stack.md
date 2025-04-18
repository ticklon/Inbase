# 技術選定 - Inbase

## フロントエンド（iOSアプリ）
- **言語**: Swift
- **UIフレームワーク**: SwiftUI
- **対応OS**: iOS 15以降

## OCRライブラリ
- **Apple Vision Framework**
  - iOS標準のOCRライブラリ
  - ローカル処理でセキュア
  - 表形式や複雑なレイアウトには補助処理を加える可能性あり

## PDF・画像処理
- **PDFKit**：PDFファイルの読み込み、ページ表示、抽出など
- **UIKit（併用）**：画像選択（UIImagePickerController）に必要な場面で利用

## JSON管理
- **Codable構造体（Swift標準）**
- **FileManager** によるローカルファイルの保存・読み込み

## 状態管理・データ管理
- **@State / @ObservedObject / @StateObject**：SwiftUIの状態管理機構を活用
- **Combine（必要に応じて）**：リアクティブプログラミング支援

## テスト・検証
- **XCTest**：単体テスト用
- **Preview機能**：SwiftUIプレビューでUI検証

## 将来的な拡張性を考慮して検討中
- iCloud連携
- CoreData or SQLite対応（構造化データの高速検索・保存）
- 外部共有・PDFエクスポート機能
- バックアップ/リストア機能

## 不採用候補（今回の要件には不要）
- Firebase, Realm：クラウド依存や外部DBが不要なため使用しない
- Flutter, React Native：iOS専用のためネイティブ(Swift)を優先


