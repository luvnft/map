# Lightning Map
This project is a map website mostly for merchat collection & display of places that accept Lightning Network in Prague, Czech Republic.  

## Run it!
```
git clone https://github.com/KlosStepan/Lightning-map
npm install
npm start
```
## Preview
Everybody will be able to Register / Sign Up With Google to add pin to our map soon! 
<p align="center">
  <img src="src/img/lnmap_preview3.png" alt="lnmap_preview"/>
</p>

## Design
These colors are used in our application: 
- Black ![#000000](https://via.placeholder.com/15/000000/000000?text=+) `#000000` - normal.
- Orange ![#F7931A](https://via.placeholder.com/15/F7931A/000000?text=+) `#F7931A` - Bitcoin.
- Purple ![#2C0073](https://via.placeholder.com/15/2C0073/000000?text=+) `#2C0073` - Lightning.

Symbols for background (their 32x32 icon `png` equivalent in ![#F6F8FA](https://via.placeholder.com/15/F6F8FA/000000?text=+) `#F6F8FA`):
- Bitcoin ₿ (12.5deg. rot).
- Lightning ⚡.
- Satoshi <img src="src/img/sat.jpg" alt="alt text" width="30"/> (12.5deg. rot.).  

Logo edits like https://shallowsky.com/blog/gimp/gimp-black-to-color.html
___
## // Map fiddle
For map we use service called Mapbox wrapped for ReactJS installed as npm package. 
```jsx 
// eslint-disable-next-line import/no-webpack-loader-syntax   
mapboxgl.workerClass = require("worker-loader!mapbox-gl/dist/mapbox-gl-csp-worker").default;  
```

___ 
## // Build&push
First run to build and then push into Dockerhub/
```
docker build -t stepanklos/lightning_map .
```
```
docker push stepanklos/lightning_map
```