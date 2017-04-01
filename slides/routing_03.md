### Routing

* "resources"や"namespace"も使える

```ruby
get '/hello', to: endpoint
get '/', to: 'home#index', as: :home
get '/books/:id', to: 'books#show'

resources :books
resources :books, only: [:new, :create, :show]
resources :books, except: [:index, :edit, :update, :destroy]

namespace 'docs' do
  get '/installation', to: 'docs#installation'
  get '/usage',        to: 'docs#usage'
end
```
* Railsのroutingの書き方に大分近い
