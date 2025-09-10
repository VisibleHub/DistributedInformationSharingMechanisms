# VisibleHub - Distributed Information Sharing Mechanisms
Prototype spec for a decentralized, privacy-preserving info sharing framework.  Covers network layer, app framework, and app specs to enable anonymous and trustworthy communication.

# 分散型情報共有機構 - アーリーアクセス仕様書（第0版）  
Decentralized Information Sharing Framework - Early Access Specification (v0.0)

---

## 0.1 概要 / Overview

### 日本語

本仕様書は、セキュアで秘匿性の高い分散型情報共有機構の設計と、ネットワーク部、アプリケーションフレームワーク、各種アプリケーション仕様を構成要素としてまとめたプロトタイプの仕様を記述しています。  
本機構は、匿名性を維持しながら、信頼性のあるユーザー間情報共有を実現することを目的としています。

### English

This early-access specification describes a prototype architecture for a decentralized information-sharing system designed to be secure, privacy-preserving, and resistant to tampering or surveillance.

The system consists of:
- A secure and anonymous peer-to-peer network layer
- A cryptographically authenticated application framework
- Modular applications (e.g., decentralized social platforms, forums)

Its primary goal is to enable trustworthy information exchange among users while maintaining strong anonymity and data integrity.

---

## 0.2 システム構成 / System Architecture

### セキュアなネットワーク部 / Secure P2P Network Layer

**日本語**  
- 分散型P2P通信プロトコル  
- 暗号化と匿名化通信（IP隠蔽、ランダム化）  
- ブロックチェーンによるメッセージ整合性の担保  
- ノード数に応じた接続最適化  

**English**  
- Fully decentralized peer-to-peer communication protocol  
- End-to-end encryption using asymmetric cryptography  
- Network anonymization: IP obfuscation, dummy traffic, randomized routing  
- Blockchain-based message integrity and non-repudiation  
- Dynamic node management for optimized connections  

### アプリケーションフレームワーク / Cryptographic Application Framework

**日本語**  
- 公開鍵暗号ベースの認証  
- 信頼スコアの管理と評価  
- アクション履歴はブロックチェーンに記録  

**English**  
- User authentication via public/private key pairs  
- All actions (posts, evaluations, comments) are cryptographically signed  
- Trust evaluation system supports both positive ratings and counter-ratings  
- All activity is immutably recorded on a blockchain ledger  

### アプリケーション仕様 / Application Layer

**日本語**  
- 分散型SNS、掲示板  
- 不正利用に対応する不活性化機能  

**English**  
- Supports applications such as decentralized social media, forums, and collaborative platforms  
- Trust-based visibility and moderation mechanisms  
- Includes a deactivation mechanism to mitigate account compromise or abuse  

---

## 0.3 詳細構成 / Component Details

### 1. ネットワーク部 / Network Layer

- P2Pオーバーレイネットワークにより匿名性を確保  
- 公開鍵暗号による通信の暗号化  
- トラフィック匿名化（ダミーパケット、ランダム化）  
- ブロックチェーンによる改ざん防止と履歴保持  

**English**  
- P2P overlay network with dynamic peer connections and anonymous routing  
- Message encryption using public key cryptography  
- Traffic obfuscation using dummy packets and randomized intervals  
- Immutable logging of messages and actions using blockchain  

### 2. アプリケーションフレームワーク / Application Framework

- 公開鍵によるID管理（個人情報は不要）  
- 評価と逆評価に基づく信頼度管理  
- すべての操作は署名され、公開鍵と結びつけられる  

**English**  
- Cryptographic identity based solely on public keys  
- Bidirectional trust evaluation system with counter-evaluation feedback  
- All actions are digitally signed and linked to persistent cryptographic identities  

### 3. 各種アプリケーション / Applications

#### 分散型SNS / Decentralized Social Network

- 投稿・コメントに署名を付与し改ざんを防止  
- 信頼度に応じた表示制御や可視性の調整  

**English**  
- Posts and comments are signed to ensure authenticity  
- Content visibility is influenced by user trust levels  

#### 掲示板 / Forum

- 公開鍵で署名された投稿と、信頼スコアに基づく表示順位制御  
- 不正なユーザーや投稿は自動的に評価によって抑制される  

**English**  
- Forum threads are governed by trust-weighted visibility and ranking  
- Malicious actors are automatically down-ranked via the reputation system  

#### 不活性化機能 / Deactivation Mechanism

- アカウント乗っ取りや不正使用に対応し、主鍵を無効化可能  
- 再登録は可能であり、システムの健全性を保持  

**English**  
- Allows users to deactivate their compromised private keys  
- Enables secure re-registration while protecting system integrity  

---

## 0.4 セキュリティとプライバシー / Security & Privacy Considerations

### セキュリティ / Security

- 公開鍵暗号によるエンドツーエンド暗号化  
- すべてのデータはブロックチェーンで改ざん防止  

**English**  
- End-to-end encryption via public key cryptography  
- All data is tamper-proof via blockchain-based logging  

### プライバシー / Privacy

- 個人情報不要、公開鍵のみで認証と管理  
- トラフィック匿名化と匿名ルーティングで追跡困難  

**English**  
- No personally identifiable information is required  
- Network traffic is anonymized and unlinkable  

---

## ライセンス / License

TBD（To Be Determined）  
This project is currently under early development and the license will be specified in a future release.

---

## ステータス / Development Status

このリポジトリはアーリーアクセス版（第0版）であり、仕様は今後変更される可能性があります。議論・フィードバックを歓迎します。  
This repository is in an early-access state (v0.0) and subject to change. Community discussion and feedback are highly welcome.


---

---

## システム構成概要（Three-layer Model）

| Layer | Description | Key Functions | Related Technologies |
|-------|-------------|---------------|-----------------------|
| **1. Network Layer** | Secure P2P overlay with dynamic, anonymous routing | - Encrypted block-based messaging<br>- IP obfuscation<br>- Tamper-proof logging | Tor, Winny, DHT, Blockchain |
| **2. Application Framework** | Identity/authentication via public keys, no personal data | - Signed actions<br>- Reputation scoring with reverse evaluation<br>- Trust graph maintenance | RSA/ECC, Web of Trust, ZKP (future) |
| **3. Applications** | Modular apps like forums and social platforms | - Signed posts and comments<br>- Trust-based visibility control<br>- Deactivation against abuse | Mastodon, Secure Messaging |

---

## Key Innovations

- Fully decentralized: no central server, not even for key registration or relay
- Trust without identity: No email, name, or IP ever required
- Robust to abuse: Deactivation keys and reverse trust systems deter malicious actors
- Modular by design: Applications can be built atop the framework without network-level changes

