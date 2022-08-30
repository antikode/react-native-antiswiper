# AntiSwiper

## Installation

with npm :

```shell
  npm i react-native-antiswiper
```

with yarn :

```shell
  yarn add react-native-antiswiper
```

## Usage

```javascript
...
import AntiSwiper from 'react-native-antiswiper';

const App = () => {
    const itemWidth = 300;
    const itemHeight = 200;
    const data = [
        'https://source.unsplash.com/random?city,night',
        'https://source.unsplash.com/random?city',
        'https://source.unsplash.com/random?night',
    ];

    const [index, setIndex] = useState(0);

    const renderItem = ({ item, index }) => {
        return (
        <View
            style={{
            width: itemWidth,
            height: itemHeight,
            }}>
            <Image
            source={{ uri: item }}
            style={{ width: itemWidth, height: itemHeight, borderRadius: 8 }}
            />
        </View>
        );
    };

    return (
    <SafeAreaView>
      <AntiSwiper
        data={data}
        renderItem={renderItem}
        width={itemWidth}
        height={itemHeight}
        auto={true}
        duration={2000}
        space={16}
        horizontal={true}
        contentContainerStyle={{ marginHorizontal: 16 }}
        indicatorStyle={{ marginHorizontal: 12 }}
        index={index}
        setIndex={setIndex}
      />
    </SafeAreaView>
  );
}
```

## Contributors

[@Sardi Kapilano](https://www.github.com/sardik) [@Imam Holid](https://www.github.com/im-holid) [@Andika Andriana](https://www.github.com/andika-andriana) [@Rahmat Hidayat](https://www.github.com/rahmat1929)
