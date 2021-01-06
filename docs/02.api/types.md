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

## GenesisAsset

用于表示创世块参数

```typescript
interface GenesisAsset {
  // 链名
  chainName: string;
  // 链主权益名
  assetType: string;
  // 链网络标识符
  magic: string;
  // 链网络类型
  bnid: "b" | "c";
  // 链创世时间
  beginEpochTime: number;
  // 链创世域名
  genesisLocationName: string;
  // 链创世账户初始持有的主权益量
  genesisAmount: number;
  // 链事件每字节需要支付的最小手续费（分数）
  minTransactionFeePerByte: Fraction;
  // 链上事件体最大字节数
  maxTransactionSize: number;
  // 链上区块体最大字节数
  maxBlockSize: number;
  // 链上区块体最大处理的事件
  maxTPSPerBlock: number;
  // 删除分叉时至少需要落后的高度
  consessusBeforeSyncBlockDiff: number;
  // 每轮能处理的注册受托人数量
  maxDelegateTxsPerRound: number;
  // 权益赠送事件最大可抢次数
  maxGrabTimesOfGiftAsset: number;
  // 发行数组资产的账户最小持有的链资产数量
  issueAssetMinChainAsset: number;
  // 注册创世块的账户最小持有的链资产数量
  registerChainMinChainAsset: number;
  // 最大的过期区块间隔数量
  maxApplyAndConfirmedBlockHeightDiff: number;
  // 每轮的区块数量
  blockPerRound: number;
  // 创世受托人数量
  delegates: string[];
  // 是否允许受托人连续参与竞选
  whetherToAllowDelegateContinusElections: boolean;
  // 区块间隔
  forgeInterval: number;
  // 奖励分配比例
  rewardPercent: {
    // 投票占区块总奖励的百分比
    votePercent: Fraction;
    // 打块占区块总奖励的百分比
    forgePercent: Fraction;
  };
  // 区块链端口号
  ports: {
    // 共识端口号
    port: number;
    // 节点扫描端口号
    scan_peer_port: number;
  };
  // 区块奖励
  rewardPerBlock: {
    // 奖励变动的区块里程
    heights: number[];
    // 每个区块里程对应奖励的资产数量
    rewards: string[];
  };
  // 账户参与度权重比
  accountParticipationWeightRatio: {
    // 账户上一轮末持有的主权益量的权重
    balanceWeight: number;
    // 账户上一轮事件量持有的
    numberOfTransactionsWeight: number;
  };
  // 区块参与度权重比
  blockParticipationWeightRatio: {
    // 账户上一轮末持有的主权益量的权重
    balanceWeight: number;
    // 账户上一轮事件量持有的
    numberOfTransactionsWeight: number;
  };
  // 构建 tpow 的难度系数
  averageComputingPower: number;
  // tpow 豁免的区块高度
  toowOfWorkExemptionBlocks: number;
  // tpow 配置
  transactionPowOfWorkConfig: {
    // 链的 pow 难度增长系数
    growthFactor: Fraction;
    // 链的 pow 计算参与比率
    participationRatio: Fraction;
  };
  // 新注册的受托人
  newDelegates: string[];
  // 投票账户上轮末最大主权益量
  maxBeginBalance: number;
  // 上一轮投票账户中最大的事件量
  maxTxCount: number;
  // 下一轮的打块账户列表
  nextRoundDelegates: NextRoundDelegate[];
}
```

## RoundLastAsset

用于表示轮末块信息

```typescript
interface RoundLastAsset {
  // 新注册的受托人
  newDelegates: string[];
  // 上一轮投票账户中的最大轮末主权益量
  maxBeginBalance: number;
  // 上一轮投票账户中最大的事件量
  maxTxCount: number;
  // 下一轮的打块账户列表
  nextRoundDelegates: NextRoundDelegate[];
  // 链上链hash
  hash: string;
  // 上一轮投票账户的最大轮末主权益量和上一轮投票账户的最大事件的比
  rate: any;
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

## GetAccountAccountInfo

调用 GetAccountInfoAndAssets 接口的时候返回的 accountInfo 字段类型描述

```typescript
interface GetAccountAccountInfo {
  // 账户地址
  address: string;
  // 账户公钥
  publicKey?: string;

  username?: string;
  // 账户状态 0 为正常；1 为冻结状态
  accountStatus: number;
  // 是否为受托人：false 为普通账户；true 为受托人
  isDelegate: boolean;
  // 是否接收投票：false 为不接收；true 为接收投票
  isAcceptVote: boolean;

  secondPublicKey?: string;
  // 已锻造区块数
  producedblocks: number;
  // 掉块数量，被选为受托人并且到达锻造区块的时间却因为各种原因没有锻造出相应的区块的次数
  missedblocks: number;

  voteInfo: {
    // 获得的权益所属轮次
    round: number;
    // 获得的权益数量
    vote: bigint;
  };

  equityInfo: {
    // 权益所属轮次
    round: number;
    // 权益剩余值
    equity: bigint;
    // 权益初始值
    fixedEquity: bigint;
  };
  // 上一轮的余额信息， 倒数第一轮的轮次信息，若当前为 600 ，则当前为第 11 轮，这个值指的则是第 10 轮
  lastRoundInfo: {
    // 轮次
    round: number;
    // 轮末账户持有的主权益数量
    assetNumber: bigint;
    // 本轮账户的事件量
    txCount: number;
  };
  // 账户变动高度
  height: number;

  productivity?: number;
}
```

## GetAccountAccountAsset

调用 GetAccountInfoAndAssets 接口的时候返回的 accountAsset 字段类型描述

```typescript
interface GetAccountAccountAsset {
  // 地址
  address: string;
  publicKey?: string;
  assets: {
    [sourceChainMagic: string]: {
      [assetType: string]: {
        // 权益所属链网络标识符
        sourceChainMagic: string;
        // 权益名称
        assetType: string;
        // 权益所属主链名称
        sourceChainName?: string;
        // 权益数量
        assetNumber: bigint;
        penultimateRoundInfo?: {
          round: number;
          assetNumber: bigint;
          txCount: number;
        };
        lastRoundInfo?: {
          // 轮次;
          round: number;
          // 轮末账户持有的主权益数量
          assetNumber: bigint;
          // 本轮账户的事件量
          txCount: number;
        };
      };
    };
  };
  // 累计花费手续费
  paidFee: bigint;
  // 累计投票收益
  votingRewards: bigint;
  // 累计打块收益
  forgingRewards: bigint;
  // 账户变动高度
  height: number;
}
```
