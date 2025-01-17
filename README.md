Commits
#1 - initial commit. Setup and tailwig config.


#2. created components folder. Created Navbar.jsx. Setup initial Navbar component. Created Footer.jsx and created initial Footer component. Created Loader.jsx and initial Loader component. Created Showcase.jsx and setup initial Showcase component. Created Transactions.jsx and setup initial Transactions component. Created Hero.jsx and setup initial Hero component. Created Services.jsx and setup initial Services component. Created ImgBox.jsx and setup initial component. Created BookBox.jsx and setup intial component. Setup Form.jsx and initial component. After the initial components were created I created index.js file and exported each component from that file.

#3. Imported in the Navbar, Hero, Showcase, Skills, Services and Footer components into index.js. Forgot to make Skills.jsx so made that and setup initial component then added to the index.js export file. Created _document.js and setup according to NextJS documentation to allow Google Fonts import. Added a head component with a title to pages/index.js.

#4. Installed npm react-icons package. Imported two react icons for the open/close menu bar. Created a photos folder inside of public folder. Brought in a logo and imported it to the Navbar component after compressing. Installed npm ethers package for blockchain manipulation. Imported useRouter inside the Navbar and used it to push to sprucey.dev when the logo is clicked. 

#5. Created the NavItem component and inserted into the Navbar component. Mapped over an array of made up links to populate the navbar for non-mobile. For mobile set up a useState, toggleMenu, to monitor if the menu is toggled to open or close. Setup conditional rendering of the menu buttons depending on useState value. Laid out basic structure of navigation and open/close menu functionality.

#6. Added in a favicon.ico inside pages/index.js. Created data folder. Created data.jsx inside of it. Created an array of objects containing the data for each navigation link. Imported data into Navbar.jsx and replaced the []'s with the imported links and mapped over them instead. Did more styling to the navbar - replaced icons, changed colors, changed font, changed text positioning when menu is open, and added background effects during menu open as well.

#7. I created Menu.jsx inside of components and extracted the menu portion of the return from Navbar. Then I imported the new component into Navbar and made the same as before. Created hooks folder inside of components. Created NavContext.jsx inside of that and set up a NavbarContext/Navbar.Provider so that I can pass the state about the menu being toggled open or close between the Navbar component and the Menu component from the context instead of occupying both components with redundant state.

#8. The menu functionality was not working correctly so I added another conditional inside of the MobMenu.jsx file which was renamed from Menu and updated around the app. I removed the useContext until this bug was sorted and now will hook up the same functionality using the useContext hook on the next update. Still need to add background affects and change text positioning when MobMenu is open.

#9. Connected the useContext hook and achieved the same functionality as before.

#10. Brought in a minimized photo and set as the bg image for the mobile menu. Brought in and styled GitHub and Twitter icons. Finished mobile menu until final tweaks.

#11. Did lots of styling tweaks to the navbar to make it responsive and correct on mobile, medium and large screens. The Navbar setup is now finished excepting for final touches and connecting the links & connect button.

#12. Did more style changes to Navbar.

#13. Started work on the Hero component. Brought in 3 react icons. Imported the Loader component to use during data fetching. Added in some Hero text and styled. Added in a button type button for mobile to connect wallet. Started set up of the connect button's onClick function connectWallet. Added a radial gradient generated from css.hero as well as a glassmorphism. Added a future component which will be the cryptocard displaying user TX's.

#14. Worked on setting up the cryptocard with hardcoded values/icons. Added a json.config file and set the compiler options to use smart file routing. Created CCard.jsx inside of components and extracted the cryptocard there. Then imported back into the Hero and inserted.

#15. Created Input component inside Hero.jsx. Used it to populate the Hero with multiple input fields inside the return. Set up the initial state for a Loader component. Created a new state to monitor whether isLoading is set to true or not. The render is conditonal with either a loader message or a button. Setup the handleSubmit function used as an onclick inside the conditionally rendered button. Created Input.jsx and moved the form into there before extracting back into the Hero.

#16. Styled Send Now button. Set up Loader component and imported to the hero for use. Brought in an outside loader from spinkit. Brought in a hero image and set as the background. Did some styling adjustments to suit the adjustment.

#17. Created new smartContract folder and cd'd into. npm i hardhat @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ether packages. Used Hardhat for the smart contract development to create new setup. Created Payments.sol. Created Payments contract. Created Payment event. Created PaymentStruct to give properties to our payments.

#18. Created a payments array to store all transaction objects. Created addToChain, getAllTXs, and getTXCount functions.

#19. Renamed sample-scripts.js to deploy.js inside of scripts folder. Cleaned up file. Created runMain function. Set up to deploy Payments.sol. Used Ropsten test faucet to acquire some ETH for contract testing. Used Alchemy to set up a testing network. Deleted hardhat.config.js file and recreated for my needs. Deployed to ropsten network using hardhat: npx hardhat run scripts/deploy.js --network ropsten. 

#20. Created utils folder. Created constants.js. c&p Payments.json into utils/Payments.json (new file). Imported abi from Payments.json. Exported contractABI and contractAddress. Created new context folder. Created PaymentsContext.jsx inside of it.

#21. Started setting up PaymentsContext. Imported ethers and the contractABI and contractAddress. Created getEthereumContract function. Settup the PaymentsProvider. Wrapped around app inside of _app.js. Imported the context into Hero.jsx. Deleted context folder and moved PaymentsContext.jsx into the providers folder. Created isWalletConnected function. Setup a useEffect to run isWalletConnected. Started setup - console logged active account.

#22. Setup functionality for connect metamask button inside of the context file. Did this using connectWallet function. Created a new state, currentAccount/setCurrentAccount to keep track of active user accnt. Passed connectWallet to Hero.jsx and used inside with the button. Also connected the same functionality on the navbar button for large screens as well. Both buttons open the metamask wallet extension.

#23. Set to ensure the active account always starts with account0. Conditionally rendered the connect button to disappear on small screens when actively signed in. Changed button text on nav button during sign in for larger screens.

#24. Created sendPayment function. Created new state formData/setFormData to deal with importing form fields. Created handleChange function, passed through context. Finished handleSubmit function. Added a useState isLoading/SetIsLoading for the hero page during blockchain transactions. Created new useState transactioinCount/setTransactionCount to monitor the number of transactions.

#25. Downloaded npm i @metamask/detect-provider to replace the current window method of doing things. Was implementing provider based on React method - NextJS does not have window object due to server-side nature. Will redo from scaratch later after site is built out. This commit I built out the showcase component. I added an array of objects to the data.js page and used that to hold the data for each seperate showcase component. Then I mapped over the data inside of Showcase.jsx in order to render the three showcase cards with data dynamically inserted.

#26. Finished styling the showcase cards. Added a state variable readMore/setReadMore for the showcase cards to keep the cards the same length regardless of description size. Created SingleCard.JSX to conditionally render an extra showcase card on larger screens. Also created a HeroContext.jsx to keep control of the readMore/setReadMore state variable which is being used by both Showcase and SingleCard.

#27. Styled showcase cards. Finished excepting for the conditional rendering. Added skills to data.jsx for rendering to the SkillsList component. Built out skills list component and added heading to showcase and table. Imported two icons for the skillsets component. Finished skillsets component.

#28. Started Services component. Created cards and displayed with styling. Also constructed the footer component as well. Got both components set up and started styling.

#29. Finished styling the Services and Footer components. Finished styling most of the main page with responsive design.

#30. Finished styling the main home page for all screen sizes. All finished. Then created Modal.jsx and started creating a modal component. Finished the modal component and did a ton of styling for all the screen sizes. Finished completely the page. Forgot to commit to get Git and already started the about page. Imported the Navbar and Footer components, set the bg, and now am preparing to work on the Main component.

#31. Created Profile.jsx component and completed. Then added a new array of objects to data.js containing the images for the ImgBox component.

#32. Constructed the ImgBox component. Created images/setImages useState to keep the image data. Created index/setIndex to keep track of images in the slide. Mapped over images.

#33. Finished ImgBox component. Used a useEffect to handle the last slide in the array. Created the 2nd useEffect for the autoslide functionality. Finished all styling and adding in the picture data. Component complete.

#34. Started on BookBox component. Used WebViewer to allow PDF embedding into the component using npm install @pdftron/webviewer --save. Copied public and core folders from node_modules into this project and paste them inside the public folder. Created new folder inside public called lib (library) and put ui and core folders inside it. Finished setting up the embedded pdf document - used imported code from the webViewer docs. Did styling. Component finished.

#35. Started on Blog.jsx. Added blogsPost data into the data.jsx file. I do not want to add unneccessary task to this project and so for now instead of converting all of the blogs I have into markup and then building out a blog component I will simply reuse the slider component from the images and allow the post to be selected and red by button click. Will rerender using a markup built component after the next project is finished which actually requires one and it is not critical that this one be like that before launch. To do this I brought in the readMore/setReadMore from the HeroContext to use to toggle the button to display the full length text. Styled the buttons and card to make different from the slider above. Component finished.

#36. Added and styled the WhatElse component. Created WhatElse.jsx to do so. Also added toggleMenu from the NavigationContext to keep the Profile, ImgBox, and Bookbox from being displayed on the mobile menu.

#37. Carried out the styling changes for responsive layouts. Finished the About page.

#38. Created contact.js page. Downloaded npm i react-tsparticles. Downloaded npm install @emailjs/browser. Styled Contact page for responsive viewing. FRONT END OF SITE IS FINISHED - excepting for a change to the layout for the about page which will need to be redone but which I will do after building out the backend first.

#39. Created jsconfig.json file in root and created new compiler options to allow path aliases for each of the folders, components, public and style. Then went and changed the routes to the new form using @.

#40. Created Web3Provider.jsx inside of providers folder. Created a ui folder inside of components folder. Moved all UI/layout component files into that folder. 

#41. Created web3 folder inside of providers folder. Created index.js to relace Web3Provder.jsx. Created Web3Context. Inside index.js I set up another useContext. Exported the finished context as useWeb3() function. Wrapped the application inside the Web3 provider. Tested the context to make sure props were passed successfully.

#42. Already have metamask provider installed. Installed npm i web3 as well. Created a useEffect to load the provider and web3Api/setWeb3Api as new state variables to keep the key/values stored. Setup the web3Api and passed it through the context as a child.

#43. Deleted the old PaymentsProvider and the smartContracts directory. Will start from sctratch. Tested provider and for web3 being loaded - test successful. 

#44. changed isInitialized to isLoading, changed the values around. Connected MetaMask to the connect buttons. Did this using useMemo and eth_requestAccounts. bug occurs bc only can open Meta once from click before error due to ongoing process. Fixed with location.reload().

#45. Conditionally rendered messages for the wallet connect buttons depending on if web3provider is loading/present or not. Created isWeb3Loaded property inside _web3Api.

#46. Created button folder and index.js inside of it. Created Button component. Swapped out button/> for Button/> inside Hero and Navbar. Added another conditional to the ternary operators (made dbl ternary) to display a loading message on the button during web3 init.

#47. Disabled the button during certain condition. Extended tailwinds functionality in config.js to allow opacity to accept disabled as a property. Same for the cursor. Set disabled to the connect meta buttons during web3loading state. Set the install metamask buttons to direct to the metamask homepage using onclick handlers.

#48. Got the active metamask user as well as the chain id to determine what chain is connected. Created hooks folder inside of web3 folder. Created useAccount.js inside. Also created setupHooks.js in same folder. Created setupHooks function. Embedded hooks into the provider. setHooks takes web3 which it uses to call useAccount with web3 as the parameter which will then be built out next to actual retrieve the active metamask user account.

#49. Created web3 folder inside components. Then created folder called hooks. Then created useAccount.js. Created setupHooks() inside of the web3 provider. succesffuly pssed the useAccount hook to the hero, currently is just a string of text.

#50. Added use state to handlerToGetUserMetaAccnt function to keep track of current meta account user. Created a useEffect in same function to create side effects to get accounts using getAccount. Successfully displayed to UI.

#51. Changed connect button text to display greeting to signed in user by amending the ternary ops in hero and navbar. Hooked up the useAccount to display to the CCard component. Removed button display from hero during sign in since is redundant with the ui card display.

#52. Setup handlerToGetUserMetaAccnt to rerender on account changes. Did this using another useEffect inside of useAccount.js.

#53. Used swr package to handle data fetching instead of current useEffect scheme. npm i swr.

#54. Added admin property to the use account to display admin greeting or guest greeting in ui. Setup admin account to TESTING account using adminAddresses. 

#55. Hashed the admin address for adminAddresses using keccek256. Changed file tree. Created new hooks folder inside components and then inside hooks created web3 folder. Moved useAccount.js from the web3/hooks into the hooks/web3 folders and then deleted the web3/hooks folders.

#56. Begin setting up the finctionality to display the active network to the CCard component. Created useNetwork.js inside of web3/hooks. Created useNetwork.js in hooks/web3. Successfully rendered the test message into the ccard.

#57. Worked to display actual network to UI. Used swr inside of the useNetwork file to fetch the network id. Created a useEffect to update changes to the network in the UI. 

#58. Small UI fix - during network change hexadecimal is displayed before numeric value for network id. Used partInt on the mutated value to fix. Created object of network id's with maps to string to display names instead of id's to the UI. 

#59. Set up UI message to display when user is on wrong network. Created .env dev and prod files for default chain id. Created targetNetwork variable. 

#60. Finished setting up the UI message using the isSupported and network.target properties. Combined useAccount and useNetwork hooks into newly created index.js file. Then deleted old files. Created enhanceHook function to add the hasInititialResponse property to the swrResponse of useNetwork/useAccount.

#61. Current setup leaves setupHooks function called many times. To improve removed getHooks from the _web3Api and added to the web3Api state variable to reduce function calls. 

#62. Reconfigured ternary operators for the hero/nav button to use requireInstall instead of web3 to prevent unneccessary importing.

#63. Created useEthPrice.js to get price of ETH for app. created fetcher function to pull api data from coingecko api using useEthPrice function. Retrieved json data. 

#64. Displayed the ETH price to the ui in Hero. Repeated process for FTM and XMR. Set up refreshInterval to refresh values to UI every 1 minute.

#65. Displayed SPIRIT, BTC, and SCRT prices to UI, imported logos. Did some styling.

#66. Added functionality to the payment inputs. Created makePayment object and paymentData/setPaymentData useState. Successfully alerted form data on submit.

#67. Set up validations for inputs using createFormState function. Added loaders to token api call values during fetches.

#68. Ran truffle init. Prepared tuffle-config file. Created ProfilePayments.sol. Created 2_profile_migration.js. Ran truffle migrate. Added truffle-config to Ganache and verified ProfilePayments deployment. 

#69. Set up contract owner using setContractOwner and constructor. Made contract payable.

#70. Created getContractOwner function to get contract owner. Created transferOwnership function to transfer contract ownership. Tested on Remix.

#71. Created onlyOwner modifier to restrict function access to msg.sender whenever used. Created onlyOwner error. 

#72. Ran truffle migrate --reset. Deleted build folder from improper compiler command. Fixed compiler. Ran truffle compile, now contracts in public folder. Created utils folder in root. Created loadContract.js and updated jsconfig.json for new route. Installed npm i @truffle/contract. Imported contract from truffle/contract. Created loadContract function. Added the contract into the provider. NextJS causes issues with fs package.. NextJS compiles server version instead of browser. 

#73. Instead of editing next.config or pasting minfied file directly into browser. ran npm uninstall @truffle/contract --- too large. Loaded the contract using web3 instead. Added new env variable for network id.

#74. Refactored enhanceHook function. Created _isEmpty function to check for empty data being returned for either useAccount or useNetwork hooks.

#75. Handled empty accounts[]0 from being returned as undefined in useAccounts.js by amending the handler function to return an error in that instance. Repeated the same process for useNetwork.js.

#76. Refactored the useEffect in useAccounts and useNetwork to remove the account/chainChanged listeners during unmounting to avoid repetitive function calls.

#77. Created ProfilePayments.test.js. Set up initial testing enviornment. Ran truffle test, no errors. Imported a catch revert file to replace try/catch blocks in testing file and serve exceptions.

#78. Setup testing for transferOwnership SC function. Ran truffle test, all passed.

#79. Created a getGas abstraction for use with withdrawl/send payment transactions. Created getBalance and toBN functions as well.

#80. Created stopContract and resumeContract functions to shut down/restart SC after deployment if required. Created onlyWhenNotStopped modifier.

#81. Created functionality to allow funds to be sent to the SC along with withdrawal ability using receive and withdrawal functions. Created emergencyWithdraw function. Created selfDestruct function to erase SC from chain.

#82. Ran truffle migrate --reset. Sent test ether to contract via Meta, success - verified in Ganache. Created testing for TX before/after amount. Passed in truffle test.

#83. Tested withdrawl functionality with new testing. All passed.

#84. Created testing for emergencyWithdrawal function. All passed.

#85. Created testing for the selfDestruct function. All passed.

#86. Prepared truffle ropsten config besides mnemonic and api. Installed npm i @truffle/hdwallet-provider.

#87. Created new project on infura. Added keys.json to .gitignore then created the named file. Added variables to keys.json. Imported keys to truffle-config and setup providerUrl.

#88. Generated mnemonic for infura/ropsten, setup in truffle-config. Confirmed working connection between Ropsten/InfuraAPI. Confirmed deployment account using const accounts = await web3.eth.getAccounts() in the truffle console. Verified deployed account balance using await web3.eth.getBalance(accounts[]0). Successful.

#89. Deployed to Ropsten test network using truffle migrate --network ropsten. Deployment successful. 

#90. Changed env file to allow ropsten to prevent UI error and make new target Ropsten. Downloaded npm i react-toastify. Set up to display toastify promise return during send payment button click.

#91. Created toast.js file. Created withToast function. Rendered to UI on click.

#92. Remade the home page for responsive screen sizes.

#93. Fixed sidebar to hide elements that were showing up through the home page.

#94. Styled About and contact pages to make responsive. Besides some refactors and a few edits I know about (button clicker), this project is done.

#95. Ran npm run build. Build completed. Uploaded to Vercel.