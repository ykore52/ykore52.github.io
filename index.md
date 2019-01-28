# Resume (職務経歴書)

## Name: Yuji Koretomo (是友 佑治)

## Summary (職務要約)

* 医療機関向け電子カルテシステムの運用 (6ヶ月)
* PHPを使ったWebアプリケーションの設計・開発および基盤サーバーの設計・構築 (1年)
* 大学・民間企業向けの情報系システムの設計・構築 (4年程度)
  * 構築プロジェクトにて5名以下のチームリーダーを経験
* 金融機関の情報系システム更改プロジェクトのベンダーコントロール業務 (2年)
* 金融機関の情報システム部門での業務支援SE (3年)
  * 担当する情報系システムの運用業務(照会対応、技術的なトラブルシューティング等)
  * 他の更改案件における技術支援等

## Experiences (職歴)

### 2008年4月～現在　日本ビジネスデータープロセシングセンター　（神戸市）

* 事業内容：ITソリューション事業、医療関連事業、公共福祉事業
* 資本金：3000万円

#### 2008.4 ~ 2008.10 : 医療機関向け電子カルテシステムのヘルプデスク兼運用SE

医療機関にて電子カルテシステムのヘルプデスクと運用業務を担当した。

#### 2010.5 ~ 2011.1 : PHPを使ったWebアプリケーションの設計・開発・テストおよび基盤サーバーの設計・構築

当初3名体制のPJで画面プロトタイプのみ出来上がった状態で参画した。担当は画面設計と開発、更に基盤サーバーの設計を担当した。
  * PHP 5.1、自社PHPフレームワーク、RHEL5

#### 2008.11 ~ 2014.3 (PHP開発PJ期間を除く) : 複数の大学・金融機関・民間企業のインフラ構築・運用業務

数名規模のセクションから数万人規模のユーザーまで、様々なプロジェクトにてインフラ基盤の設計・構築・運用を経験した。
2012年からは5名程度インフラチームリーダーを担当した。

  * RHEL5/6、Apache httpd、postfix、squid、VMware vSphere、Windows Server 2008～、System Center Configuration Manager、Zabbix、Cacti
  * 富士通製ストレージ(Data ONTAP)の設計・構築

#### 2014.4 ~ 2015.6 : 金融機関の情報系システム更改プロジェクトのベンダーコントロール業務

社内情報系システム更改プロジェクトにおけるベンダーコントロール役として参入。プロジェクトにおけるステークホルダー間の調整、技術的課題の調整、成果物(設計書等)のレビューを担当。

##### メール移行を担当

PJ終盤、受注ベンダーがメールデータ(300万件以上)の移行が出来ないというので私が担当することになった。更改前後でメールソフトが変更され、ディレクトリ構造、ファイル命名ルールや暗号化の有無が根本的に異なっており、非常に特殊な状況であったため、当初は単純に移行すると100時間以上は掛かる想定で移行スケジュール的に不可能であった。しかし、いくつかのアイデアを思いつき、移行用bashスクリプトに実装してみたところ、最終的には6時間程度に短縮することができた。
  * 前日までのバックアップに当日データとの差分を反映させることを提案するが、暗号化の仕様上 rsync を利用できなかったため、自前で差分コピー機能を実装
  * 当初は、処理の途中にあるディレクトリ構造の再構成処理にファイルコピーを行っていたが、コピーの代わりにシンボリックリンクを作成することで大幅に時間短縮
  * 処理のマルチプロセス化(並列化)

#### 2015.7 ~ 現在 : 金融機関の情報システム部門での業務支援SE・ヘルプデスク
 
社内情報系システムの運用・ヘルプデスク、ユーザー1500名程度。ユーザ管理などの業務運用における障害対応や電話照会対応等を担当。

  * Windows Server 2012～、Active Directory、RHEL5/6、postfix、VMware
  * PaloAlto PAシリーズ、FortiGate
  * Cisco製 L2/L3 Switch

##### 業務改善活動：基盤の信頼性向上・ヘルプデスク要員の業務効率化

私が着任した当初から、ユーザーからの問い合わせ対応を記録するソフトウェアとしてチケットトラッキングシステムである Trac を利用していたが、バージョンが古いものであったり、バックアップがローカル保存のみ等脆弱な部分があった。ユーザーからのリクエストを記録するソフトウェアを自社製の MS-Access アプリケーションに記録していたが、メンテナーがPJから離脱しカスタマイズが困難となったため、この部分については Redmine を新規構築し移行することとした。

Trac に関しては最新版への更新と、Trac内部データベースを sqlite から RDBMS(MySQL) への切り替え、バックアップの多重化を行った。DBのバックアップ運用には可視化という観点からジョブランナーとして Jenkins を導入した。

ソフトウェアのオペレーションが増えることから、オペレーションと構築手順の標準化による運用負荷の軽減と、将来的に基盤を更改した場合のポータビリティを向上させるため、 Docker による構築の自動化・コンテナ化を実施した。

上記の諸々の構築・設定作業はすべて私1人で担当した。

## Skills (スキル)

* Microsoft系
  * Active Directory、WSUS
  * System Center Configuration Manager

* Linux系
  * RHEL、CentOS、Debian、Ubuntu
  * httpd、postfix、squid、ISC BIND

* 仮想化
  * VMware vSphere
  * VirtualBox
  * Docker

* クラウド
  * AWS : EC2,S3などを趣味や学習として使用する程度

* プログラミング言語
  * bash、PowerShell、VBScript
  * Python
  * PHP
  * 趣味レベル
    * Python Django : 簡単なサービスを作成できる程度
    * Ruby (on Rails) : Redmineの簡易なプラグインを業務用に作成した程度
    * Go : 基本文法やツール群は理解
    * C++ : 学生時代はゲームプログラミングで使用していた
    * NodeJS : 簡単なサービスを作成できる程度
    * HTML/CSS/jQuery/Bootstrap : 簡単な UI を作成できる程度

* その他
  * Git、SVN、Jenkins、Trac、Redmine

## Education (学歴)

* 2008.3 - Bachelor of Computer Science - Okayama University of Science (岡山理科大学 工学部 情報工学科)

## Qualifications (資格)

* IPA - Software Design &amp; Development Engineer (ソフトウェア開発技術者)
* IPA - Information Security Specialist (情報セキュリティスペシャリスト)
* LPIC level 1
* TOEIC 565

## Language (語学)

* Japanese (native)
* English (entry level)

## Other

* Blog: https://ykore.hatenablog.com/
* GitHub: https://github.com/ykore52/