1.create html document (index.html)

2 create javascript file (script.js)

3 integrate html file with javascript file with the help of script tag
4 add a functionality make sure the ui comes with the expected behaviour
5  then do npm init in the folder
6 install jest jsdom packages jest-environment-jsdom @testing-library/dom
    @testing-library/jest-dom
    @testing-library/user-event
7 add the necessary scripts to it   "test": "jest --watch",
    "coverage": "jest --coverage"

8 create a file jest.config.js and a script to it
<code>module.exports = {
   
    testEnvironment:"jsdom",

   
  };</code>

9 create a file called (asyouwishfile).test.js 
<code>
require("@testing-library/jest-dom");

beforeEach(() => {
      const html = fs.readFileSync(
    path.resolve(__dirname, "../index.html"),
    "utf8"
  );
  document.documentElement.innerHTML = html.toString();
    require("../yourjsFile.js");
    jest.resetModules();
})
describe("xxxxx",()=>{
    test("write descripotion for your test",()=>{

    })
})

</code>
10 npm run test -for test 
npm run coverage - for test coverage
