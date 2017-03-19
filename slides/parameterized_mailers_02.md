### [Parameterized mailers](https://github.com/rails/rails/pull/27825)

**Before**

```ruby
class InvitationsMailer < ApplicationMailer
  def account_invitation(inviter, invitee)
    @account = inviter.account
    @inviter = inviter
    @invitee = invitee

    subject = "#{@inviter.name} invited you to their Basecamp (#{@account.name})"

    mail \
      subject:   subject,
      to:        invitee.email_address,
      from:      common_address(inviter),
      reply_to:  inviter.email_address_with_name
  end

  def bulk_project_invitation(projects, inviter, invitee)
    @account  = inviter.account
    @projects = projects.sort_by(&:name)
    @inviter  = inviter
    @invitee  = invitee

    subject = "#{@inviter.name.familiar} added you to some new stuff in Basecamp (#{@account.name})"

    mail \
      subject:   subject,
      to:        invitee.email_address,
      from:      common_address(inviter),
      reply_to:  inviter.email_address_with_name
  end
end

InvitationsMailer.account_invitation(person_a, person_b).deliver_later
```
