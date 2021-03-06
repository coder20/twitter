## Getting started
1. [Setup the project](#setup-the-project)
- [By cloning this repo and using the Github Flow](#cloning-the-repo-use-the-github-flow)
- [By downloading the entire project directory as a compressed folder](#downloading-the-project-directory)

#### Cloning the repo (Use the Github flow)
1. Clone this repository
2. Follow the [Github Flow](https://guides.github.com/introduction/flow/)
3. Complete the requirements
4. Open a pull request!

### Setup the project
1. Run npm install
2. Run `npm start` to run server
3. Open `http://localhost:3001/` in browser, if you see `Here you go!` text in the browser that means server is successfully running
4. Please find `index.html` in the `public` folder
5. Now you can start your coding!



we provide you a server which provides you with the [following api endpoints](https://github.com/Infratab/Twitter-Trends/blob/master/API.md). Our server provides trends of different countries from Twitter at some point of time. 

I have implement the following design and fulfil the functional requirements listed [below](https://github.com/Infratab/frontend-challenge#functional-requirements). You can implement the design using any library/frameworks you like or just good old plain html/css.


#### Functional Requirements:

##### 1. Select countries
The two dropdowns in the **Select countries** section provide a list of countries for the user to choose from. This list of countries is provided by [**GET /countries**](https://github.com/Infratab/frontend-challenge/blob/master/API.md#get-countries).

##### 2. Common trends
When two countries are selected by the user, the trends common to both the countries are shown in the **Common trends** section. If only one country is selected, all the trends of that country are showin in the **Common trends** section. This list of trends for a particular country is provided by [**GET /countries/{country}/trends**](https://github.com/Infratab/frontend-challenge/blob/master/API.md#get-countriescountrytrends).
 
##### 3. Trend weights contribution
A pie chart is drawn based on a few computations from the list of **Common trends**. The computations that need to be implemented are as follows -
 1. **Trend weight** is the number of characters in each of the trends i.e. the length of each "trend" string.
    
    For example, the **Trend weight** of "#thecrosspolo" is 13 which is the length of the "trend" string.
 2. Calculate the "Total trend weight" by summation of all the **Trend weights** in the list of **Common trends**.
    
    For example, the "Total trend weight" in the image provided above is 24.
 3. Calculate the **Trend weight contribution** contribution of each trend in the list of **Common trends** to the "Total trend weight" by using the following formula: [(**Trend weight**/"Total trend weight") x 100]
    
    For example, the **Trend weight contribution** of "#thecrosspolo" from the image above is [(13/24)x100] = 54.2%
