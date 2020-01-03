# Commitlint & Commitizen

## Commands
  yarn init -Y

  git init

  yarn add @commitlint/config-conventional @commitlint/cli -D
  
   ### includes at package.json
       
        "husky": {
          "hooks": {
          "commit-msg": "commitlint -E HUSKY_GIT_PARAMS",
          "prepare-commit-msg": "exec < /dev/tty && git cz --hook || true"
        }  

  yarn add husky -D

  yarn add commitizen -D

  yarn commitizen init cz-conventional-changelog --yarn --dev --exact

    ### include at package.json
  
      "scripts": {
        "commit": "git-cz"
      },

  To commit you can use
  
     yarn commit 
  
    or
  
      git commit
