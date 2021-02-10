# yearn-graph-charts



## Usage

```typescript
import { TradeChart } from '@yfi/graph-charts';
import '@yfi/graph-charts/dist/style.css';

<TradeChart
  theme="dark" // or light
  data={testData}
  granularityStr="1d"
  priceDecimals={4}
  styles={{ upColor: '#00d99f' }}
  clickCallback={result => {
    console.log('result: ', result);
  }}
  clickGranularity={result => {
    console.log('result: ', result);
  }}
/>
```

> Props

```
interface Styles {
  background?: string;
  upColor?: string;
  downColor?: string;
  axisColor?: string;
  barColor?: string;
}

interface I18nItems {
  overlay?: string;
  line?: string;
  candle?: string;
  oneDay?: string;
  oneHour?: string;
  fiveMinutes?: string;
  open?: string;
  high?: string;
  low?: string;
  close?: string;
  volume?: string;
}

interface Props {
  data: any;
  granularityStr: string; // "1d", "1h", "5m"
  priceDecimals: number;
  theme?: string;
  styles?: Styles;
  i18n?: I18nItems;
  clickCallback?: any;
  handleLoadMore?: any;
  clickGranularity?: string;
  defaultChart?: string; // 'candle', 'line'
  // start and end in the data list for current view
  start?: number;
  end?: number;
  xTickFormat?: any;
}
```

### DeepChart Example


```
import { DeepChart } from '@yfi/graph-charts';

<DeepChart
  theme="dark" // or light
  asks={bids}
  bids={asks}
  baseToken="HOT"
  quoteToken="DAI"
  styles={{ bidColor: '#00d99f' }}
  clickCallback={result => {
    console.log('result: ', result);
  }}
/>
```

DeepChart Props:

```
interface Styles {
  titleColor?: string;
  axisLabelColor?: string;
  axisColor?: string;
  borderColor?: string;
  rowBackgroundColor?: string;
  containerBackgroundColor?: string;
  askColor?: string;
  askColorArea?: string;
  bidColor?: string;
  bidColorArea?: string;
  fontFamily?: string;
}

interface I18nItems {
  midMarketPrice?: string;
  price?: string;
  cost?: string;
  sell?: string;
  buy?: string;
}

interface Props {
  bids: any;
  asks: any;
  baseToken: any;
  quoteToken: any;
  theme?: any;
  styles?: Styles;
  i18n?: I18nItems;
  priceDecimals?: any;
  amountDecimals?: any;
  clickCallback?: any;
}
```
