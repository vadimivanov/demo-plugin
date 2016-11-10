#### General Plugin overview
Plugins are extentions to currenly built 'core' (with general modules, that can not be removed) application. They expand the functionality of the application, add necessary features and are used to expand the application for users to fit their needs.   

#### Installation of the new Plugins to the application:  
1. Run the following command within your command line: npm/bower install moduleName (Module name here stands for github url for external plugin)  
*We are downloading the module from external repository*

2. To copy files from node_modules/bower_components use: webpack.config.js --> CopyWebpackPlugin, change path in it's options { from: '', to: '' }  
*Here we are copying module files from source folder to destination folder*

3. npm run copy  
*Running the copy command itself*  

4. Add module-actions.js to src/app/actions/index.js  
*here we are adding the module's actions, which are added to use them within redux architecture. The action import should look like this: http://prntscr.com/cyrh7t;

5. Add module-reducer-name.js to src/app/redux/reducer.js  
*reducer.js is redux-related file, where we add the module to redux architecture. In general, the module addition within the named file looks like this: http://prntscr.com/cyrg2z;*

6. Add actions types from module/constants/ActionTypes.js to src/app/constants/ActionTypes.js    
*The constants file contains global constants to use within an application, in general the addition to already existing 'core' constant file looks like this: http://prntscr.com/cyr9dx* 

7. Add components to src/app/index.js and src/app/index.route.js  
*To add functionality also the index.js and index.route.js files should be updated also. Within the index.js the component addition in general looks like this: http://prnt.sc/cyrb1a, where PatientBannerComponent is basically the AngularJS view name, and /rippleosi/pages/patient-details/ is the path to necessary for plugin files (listing and functionality of files for an example module are listed below);  
index.route.js is used for routing, so the application will know where to look for plugin's pages. For example, this is general view of a single plugin's code for route file: http://prntscr.com/cyrdcb, where:  
url: basically what user sees in his URL bar when he clicks on related module;  
views: list of components that will be displayed on the page after clicking on the module itself;*

#### Explanations about module functionality files, that should be developed:  
1. example-actions.js   
*This file contains actions functions for redux architecture*

2. example-reducer-name.js  
*It contains reducer functions for redux architecture*

3. example-list.component.js   
*It's list.component functionality file (angular 1.5 component)*

4. example-list.html  
*HTML template file for list.component*

5. example-detail.component.js  
*It's detail.component functionality file (angular 1.5 component)*

6. example-detail.html   
*HTML Template file for detail.component*

7. example-modal.js   
*It's modal functionality file (should be added to plugin if the modal window is necessary)*

8. example-modal.html  
*HTML Template file for modal window (should be added to plugin if the modal window is necessary)*

9. ActionTypes.js   
*This file contains actions constants for redux architecture*
