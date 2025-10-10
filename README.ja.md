# 共創型社会実現プロジェクト - Policy-as-Code

**Author:** Torisan Unya [@torisan_unya] (ORCID: https://orcid.org/0009-0004-7067-9765)

[![License: CC BY-SA 4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/deed.ja)
[![Project Status: Concept](https://img.shields.io/badge/status-concept-blue.svg)](https://github.com/torisan_unya/policy-as-code)

このプロジェクトは、誰もが政策づくりに参加できる「共創型社会」の実現を目指します。そのための革新的なアプローチとして、政策や合意形成のプロセスを、バージョン管理可能で透明性の高い「コード」として扱う **"Policy-as-Code"** の概念を提唱し、その実装を探求します。

また、人間とAIの共創を探求する研究エコシステム[Agora-Supercluster](https://github.com/torisan-unya/Agora-Supercluster)の一部でもあります。

---

## 📜 ビジョン

### なぜ、今このプロジェクトが必要なのか？

私たちの社会が直面する課題は、ますます複雑化しています。しかし、その解決策を議論し決定するプロセスは、一部の専門家や代表者に限られ、多くの市民にとっては遠い存在です。

このプロジェクトは、その「壁」を壊します。

*   **市民や活動家向け:**
    あなたの声やアイデアが、単なる「意見」で終わるのではなく、具体的な「政策案」として形になり、他の人々と協力して磨き上げられていく。そんな、民主主義の新しい形を想像してみてください。AIという強力なツールを市民の手に取り戻し、集合知によって社会を動かす未来を、私たちは目指します。例えば、近所の公園のルール作りで、住民の意見をAIが整理し、Gitでみんなが修正案を提案できるように。

*   **エンジニアや技術者向け:**
    曖昧で非構造的な政策議論を、Gitでバージョン管理し、Pull Requestで改善を提案し、自動テストで影響を予測する。そんな世界を想像してみてください。`Infrastructure as Code` がインフラ管理に革命を起こしたように、`Policy-as-Code` は社会のOSである「ガバナンス」に革命を起こす、壮大な技術的挑戦です。例えば、政策の変更履歴を追跡して、過去の失敗を防ぐ仕組み。

## 💡 "Policy-as-Code" とは？

**Policy-as-Code** とは、政策、法律、規則、合意事項などを、人間と機械の両方が解読可能な形式（コード）で記述・管理する手法です。

これにより、以下のようなメリットが生まれます。

*   **透明性:** 誰が、いつ、どのように政策案を変更したかが、`git log` のように一目瞭然になります。
*   **協調性:** `Pull Request` を通じて、誰もが改善案を提案し、オープンな場で議論できます。
*   **再現性と検証可能性:** 政策がどのようなロジックで決定されたかを誰でも追跡・検証でき、AIによるシミュレーションや影響評価も容易になります。例えば、政策の影響を数字で予測し、潜在的な問題を事前に見つける。
*   **再利用性:** 優れた政策ロジックや合意形成のパターンを、他の地域やコミュニティで再利用できます。

注意点: AIを使う際は、誤った情報（ハルシネーション）を避けるため、信頼できるデータ源を常に確認しましょう。このプロジェクトでは、そうしたリスクを最小限に抑えるガイドを入れています。

## 🚀 このリポジトリで提供するもの

このリポジトリは、"Policy-as-Code" を実現するためのツールボックスです。このプロジェクトはまずは提言として位置づけ、皆さんがこの考え方を参考に実践することをおすすめします。

*   **🤖 AIプロンプト集 ([`/prompts/ja/`](./prompts/ja/))**
    *   政策課題の分析、論点の整理、条文案の生成などをAIに支援させるためのプロンプト集。
    *   **具体例**: 「政策分析プロンプト V5.6」を使って、日本の少子化対策を分析する場合、AIに「日本の少子化対策 簡易版」と入力すると、経済・社会・政治の影響をまとめ、具体的な提案（例: 子育て支援金の配分方法）を出してくれます。詳しい使い方は[ここ](./prompts/ja/policy-analysis-v5.6.md)を参照。

*   **🛠 ツールキット (`/tools`)**
    *   政策案を構造化データに変換するスクリプトや、可視化ツールなど。
    *   **インストール方法**: Python環境で`pip install -r requirements.txt`を実行。例: `policy_to_code.py`スクリプトで、テキストの政策案をJSON形式に変換し、Gitで管理可能に。

*   **📚 ドキュメント (`/docs`)**
    *   プロジェクトの理念、チュートリアル、貢献ガイドライン。
    *   **例**: チュートリアルでは、簡単なコミュニティ規約をPolicy-as-Codeで作るステップを説明。まずは小さなグループで試してみてください。

*   **🏛️ ユースケース (`/use-cases`)**
    *   具体的な政策課題（例: 地域の公園のルール作り、オンラインコミュニティの規約改定など）にこのプロジェクトを適用した事例集。
    *   **例: 公園ルールの場合**: 住民の意見を集め、AIプロンプトで影響を分析（例: 子供の遊び場増設の経済効果）。GitでPull Requestを出し、合意形成。結果: 参加率が2倍に向上（想定シミュレーション）。

---

## License

This project is licensed under a combination of the MIT License and a patent license addendum. This structure provides legal clarity and protection for all users and contributors. The complete license agreement consists of the following two documents:

*   **[`LICENSE.md`](LICENSE.md)**: The primary copyright license (MIT License) governing the use of the software.
*   **[`PATENT_LICENSE_ADDENDUM.md`](PATENT_LICENSE_ADDENDUM.md)**: An integral addendum that grants a license to essential patent claims held by contributors.

### To Our Users

You are granted the right to use this software under the terms of the MIT License, supplemented by a patent license from all contributors, **providing enhanced legal protection and clarity** for all parties.

### To Our Contributors

Thank you for considering a contribution! Please be aware that by submitting any contribution (such as a pull request), you are explicitly agreeing to the terms of the entire license agreement, including the patent grant outlined in **[`PATENT_LICENSE_ADDENDUM.md`](PATENT_LICENSE_ADDENDUM.md)**. This is a crucial measure to protect the project, its community, and its future.


リポジトリに含まれるソースコードについては、将来的に別のオープンソースライセンス（MITなど）が適用される可能性があります。各ディレクトリの `LICENSE` ファイルをご確認ください。
