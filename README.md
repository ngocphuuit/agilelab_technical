  ### 1. Anagram Tester
  ```
  def self.anagram(word, other)
    sort_word = word.to_s.downcase.chars.sort.join
    sort_other = other.to_s.downcase.chars.sort.join
    
    if sort_word == sort_other 
      return true
    else
      return false
    end
  end
  ```
  ### 2. Domain Modelling
  ```
  namespace :manager do
    resources :answer, only: [:index, :show] do
      member do
        post 'conversation'
        get 'conversation'
        patch 'conversation'
        patch 'conversation/resolved'
      end
    end
  end
  
  namespace :employee do
    resources :answer, only: [:index, :show, :new, :created] do
      member do
        get 'conversation'
        patch 'conversation'
      end
    end
  end
  ```
  
  ### 3. Bug Fixing
  1. Check this bug and find the reason and make the scope of the error.
  2. Write TDD(Rspec, minitest) for this bug.
  3. Fix bug.
  4. Run test to check the code and bug.
  5. Test other features can be affected by this bug and fixing code. If have bug then repeat step 3,4 and 5.
  6. If bug is 'fixed' then merge it to staging environment and test again.
  7. Merge to production environment.

  ### 4. Collaboration
  1. I think the problem occur when you dont understant clearly the require of the new feature and new feature can intergrate as well with current feature or not.
     So recive and make require clearly is most important step when you want to implement new feature.
  2. If this situation have occur, I think we sould discuss about cost and time to handle and refactor the feature or create the same new feature which can intergrate whith current feature.
