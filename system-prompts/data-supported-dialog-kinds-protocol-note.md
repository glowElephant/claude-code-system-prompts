<!--
name: 'Data: Supported dialog kinds protocol note'
description: Internal protocol note describing supported request_user_dialog kinds, fail-closed behavior, and the staged-release gate
ccVersion: 2.1.169
-->
@internal Dialog kinds (request_user_dialog `dialog_kind` values) this consumer's onUserDialog can actually render. The CLI treats ABSENCE as 'cannot display' and fails closed: without the kind declared here, a dialog-gated flow degrades to its no-dialog behavior (for 'refusal_fallback_prompt', the classic refusal error) instead of parking a dialog the consumer may mishandle. First-attached-client-wins on multi-client sessions; later initializes do not change it. (The @internal tag is the staged-release gate — see the Options.supportedDialogKinds doc; delete it there and here to promote.)
