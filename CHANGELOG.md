# Changelog

## Unreleased

## [0.30.0]
- Update Telegram API to 6.3: https://core.telegram.org/bots/api#november-5-2022

## [0.29.0]
- Add SendDocument response and answer_document DSL

## [0.28.0]
- [Major] Update Telegram API to 6.2: https://core.telegram.org/bots/api#august-12-2022

## [0.27.0]
- [Major] Update Telegram API to 6.0: https://core.telegram.org/bots/api#april-16-2022

## [0.26.0]
- Update Telegram API to 5.6

## [0.25.0]
- Update Telegram API to 5.4

## [0.24.1]
- Add original API descriptions to methods and models

## [0.24.0]
- Update Telegram API to 5.3
- Breaking changes from the API:

Renamed method kickChatMember to banChatMember

Renamed method getChatMembersCount to getChatMemberCount

ChatMember now has specific subtypes (ChatMemberOwner, ChatMemberAdministrator, ChatMemberMember, ChatMemberRestricted, ChatMemberLeft, ChatMemberBanned)

BotCommandScope now has specific subtypes (BotCommandScopeDefault, BotCommandScopeAllPrivateChats, BotCommandScopeAllGroupChats, BotCommandScopeAllChatAdministrators, BotCommandScopeChat, BotCommandScopeChatAdministrators, BotCommandScopeChatMember)

## [0.23.0]
- Update Telegram API to 5.2

## [0.22.0]
- Update Telegram API to 5.1
- Add credo and fix all the issues

## [0.21.0]
- Add `{:file_content, "CONTENT", "filename.ext"}` format on `file` fields to send content directly instead of using a file path

## [0.20.0]
- Big refactor fixing bugs on the process

## [0.15.0]
- Update Telegram API to 5.0
- extractor.py now copy to clipboard the autogenerated text

## [0.14.0]
- Update Telegram API to 4.8

## [0.13.0]
- Use Supervisor.init instead of supervisor/1
- Add "description" option to `command` macro
- Add `setup_commands` option to `use ExGram.Bot` to send the commands at startup

## [0.12.0]
- Use new generator using a generic JSON

## [0.11.0]
- Update Telegram API to 4.7

## [0.10.0]
- Update Telegram API to 4.6

## [0.9.0]
- Warn when fetching token by bot's name and there are no token
- Update Telegram API to 4.5

## [0.8.1]
- Add the ability to configure custom tesla middlewares
- Fix regex macros, couldn't compile

## [0.8.0]
- Add Tesla adapter for HTTP and setting it as default
- Add ability to select Tesla adapter (tested with hackney and gun)
- Added documentation
- Added template for creating a bot

## [0.7.1]
- Fix an error when not receiving updates the local update_id keeps increasing and makes an infinite loop of retrieving updates

## [0.7.0]
- Update to BOT API 4.4
- Set a softer version in README

## [0.6.2]
- Update to BOT API 4.3

## [0.6.1]
- Update to BOT API 4.2
- Add default handle_info handler and change timeout
- Remove Supervisor.Spec uses, clean start_link and child_spec code

## [0.6.0]

- Handle when update_worker is nil and raise a better message
- Add `{:edited_message, msg}` message
- Relax hackney version
- Allow to specify JSON engine to use `config :ex_gram, json_encoder: Jason`
- Http implementation details moved from `ExGram` to `ExGram.Adapter.Http`
