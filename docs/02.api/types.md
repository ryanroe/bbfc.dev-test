# 类型定义

## Fraction

用于表示分数

```typescript
interface Fraction {
  // 分子
  numerator: number;
  // 分母
  denominator: number;
}
```

## NextRoundDelegate

用于表示下一轮受托人

```typescript
interface NextRoundDelegate {
  // 地址
  address: string;

  equity: string;
}
```

## GetBlockBlockDef

GetBlock 接口中 blocks 字段的类型定义

```typescript
interface GetBlockBlockDef {
  // 区块版本
  version: number;
  // 区块高度
  height: number;
  // 区块大小
  blockSize: number;
  // 区块时间戳
  timestamp: number;
  // 区块签名
  signature: string;
  signSignature?: string;
  // 锻造者安全公钥
  generatorPublicKey: string;
  generatorSecondPublicKey?: string;
  // 锻造者上一轮的得票数
  generatorEquity: string;
  // 上一个区块ID
  previousBlockId: string;
  // 区块奖励，单位：本；1 BFT = 100000000 本
  reward: string;
  // 区块所属链的网络标识符
  magic: string;
  // 区块参与度，区块处理的事件数据按照特定的规则计算得到的一个值。作为选取在出现相同高度的区块时的凭证
  blockParticipation: string;
  // 区块备注信息
  remark: {
    [key: string]: string;
  };
  // 区块附加信息
  asset: object;
  // 掉块地址列表
  roundOfflineGeneratersHashMap: {
    [roundOffset: string]: string;
  };
  // 交易信息
  transactionInfo: {
    startTindex: number;
    numberOfTransactions: number;
    payloadHash: string;
    payloadLength: number;
    totalAmount: string;
    totalFee: string;
    transactionInBlocks: {
      transaction: {
        timestamp: number;
        applyBlockHeight: number;
        effectiveBlockHeight: number;
        sourceIP?: string;
        nonce: number;
        subId: string;
        subEnvParams: {
          timestamp?: number;
          applyBlockHeight?: number;
          effectiveBlockHeight?: number;
          sourceIP?: string;
        };
        type: string;
        senderId: string;
        senderPublicKey: string;
        senderSecondPublicKey?: string;
        recipientId?: string;
        maxFee: string;
        rangeType: any;
        range: string[];
        dappid?: string;
        lns?: string;
        fromMagic: string;
        toMagic: string;
        remark: {
          [key: string]: string;
        };
        asset: object;
        storage?: {
          key: string;
          value: string;
        };
        storageKey?: string;
        storageValue?: string;
        version: number;
        fee: string;
        trsId: string;
        signature: string;
        signSignature?: string;
      };
      tIndex: number;
      height: number;
      transactionAssetChanges: {
        accountType: number;
        sourceChainMagic: string;
        assetType: string;
        assetPrealnum: string;
      }[];
      assetPrealnum?: {
        remainAssetPrealnum: string;
        frozenMainAssetPrealnum: string;
      };
      signature: string;
      signSignature?: string;
    }[];
    statisticInfo: {
      totalFee: sring;
      totalAsset: string;
      totalChainAsset: string;
      totalAccount: number;
      assetStatisticHashMap: {
        [index: number]: {
          magic: string;
          assetType: string;
          index: number;
          typestatisticHashMap: {
            [baseType: number]: {
              changeAmount: string;
              changeCount: nuber;
              moveAmount: string;
              transactionCount: number;
            };
          };
          total: {
            changeAmount: string;
            changeCount: nuber;
            moveAmount: string;
            transactionCount: number;
          };
        };
      };
    };
  };
}
```

## GetTransactionTrsDef

GetTransaction 接口中 trs 字段的类型定义

```typescript
interface GetTransactionTrsDef {
  tIndex: number;
  blockId: string;
  height: number;
  transactionAssetChanges: {
    accountType: number;
    sourceChainMagic: string;
    assetType: string;
    assetPrealnum: string;
  }[];
  assetPrealnum?: {
    remainAssetPrealnum: string;
    frozenMainAssetPrealnum: string;
  };
  signature: string;
  signSignature: string;
  transaction: {
    // 时间戳
    timestamp: number;
    // 事件发起高度
    applyBlockHeight: number;
    // 有效区块高度
    effectiveBlockHeight: number;
    sourceIP?: string;
    // TPOW 的随机数，TPOW：事件工作量证明机制，根据账户的权益值和账户在当前块内的事件量按照特定的规则计算生成事件的难度
    nonce: number;
    subId: string;
    subEnvParams: {
      timestamp?: number;
      applyBlockHeight?: number;
      effectiveBlockHeight?: number;
      sourceIP?: string;
    };
    type: string;
    senderId: string;
    senderPublicKey: string;
    senderSecondPublicKey?: string;
    recipientId?: string;
    maxFee: string;
    rangeType: any;
    range: string[];
    dappid?: string;
    lns?: string;
    fromMagic: string;
    toMagic: string;
    remark: {
      [key: string]: string;
    };
    asset: object;
    storage?: {
      key: string;
      value: string;
    };
    storageKey?: string;
    storageValue?: string;
    version: number;
    fee: string;
    trsId: string;
    signature: string;
    signSignature?: string;
  };
  dateCreated: number;
}
```
