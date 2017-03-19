### [Parameterized mailers](https://github.com/rails/rails/pull/27825)

**After**

```ruby
class InvitationsMailer < ApplicationMailer
  before_action { @inviter, @invitee = params[:inviter], params[:invitee] }
  before_action { @account = params[:inviter].account }

  default to:       -> { @invitee.email_address },
          from:     -> { common_address(@inviter) },
          reply_to: -> { @inviter.email_address_with_name }

  def account_invitation
    mail subject: "#{@inviter.name} invited you to their Basecamp (#{@account.name})"
  end

  def bulk_project_invitation
    @projects = params[:projects].sort_by(&:name)

    mail subject: "#{@inviter.name.familiar} added you to some new stuff in Basecamp (#{@account.name})"
  end
end

InvitationsMailer.with(inviter: person_a, invitee: person_b).account_invitation.deliver_later
```
