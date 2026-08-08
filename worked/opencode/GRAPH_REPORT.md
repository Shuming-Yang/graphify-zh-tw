# Graph Report - .  (2026-08-08)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 3903 nodes · 8701 edges · 159 communities (150 shown, 9 thin omitted)
- Extraction: 98% EXTRACTED · 2% INFERRED · 0% AMBIGUOUS · INFERRED: 153 edges (avg confidence: 0.62)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `fe82a1b6`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- session/prompt.ts
- run/types.ts
- registry.ts
- run/runtime.ts
- app-runtime.ts
- agent/agent.ts
- theme.ts
- tui/runtime.ts
- transform.ts
- provider/provider.ts
- footer.view.tsx
- httpapi/server.ts
- footer.prompt.tsx
- RunFooter
- github.handler.ts
- shared.ts
- json-schema.ts
- session-data.ts
- subagent-data.ts
- effect-cmd.ts
- api.ts
- install.ts
- run/tool.ts
- session/session.ts
- Filesystem
- lsp/server.ts
- demo.ts
- public.ts
- service.ts
- stream.transport.ts
- account/account.ts
- storage.ts
- message-v2.ts
- acp/tool.ts
- compaction.ts
- question.shared.ts
- mcp/index.ts
- errors.ts
- config/config.ts
- index.ts
- footer.permission.tsx
- formatter.ts
- server/auth.ts
- shell.ts
- tools.ts
- control-plane/workspace.ts
- middleware/workspace-routing.ts
- runtime-flags.ts
- groups/experimental.ts
- vcs.ts
- groups/tui.ts
- acp/permission.ts
- worker.ts
- markdown.ts
- bridge.ts
- groups/pty.ts
- middleware/instance-context.ts
- usage.ts
- run.ts
- installation/index.ts
- client.ts
- patch/index.ts
- server/server.ts
- question/index.ts
- McpOAuthProvider
- provider/auth.ts
- skill/index.ts
- filesystem.ts
- Subscription
- handlers/global.ts
- retry.ts
- providers.ts
- digitalocean.ts
- meta.ts
- cmd/mcp.ts
- ws.ts
- groups/workspace.ts
- plugin/index.ts
- codex.ts
- message.ts
- edit.ts
- worktree/index.ts
- toolPath
- adapters/index.ts
- authorization.ts
- Agent
- snowflake-cortex.ts
- cmd/account.ts
- copilot.ts
- native-request.ts
- directory.ts
- session-replay.ts
- cmd/tui.ts
- git/index.ts
- truncate.ts
- repo.ts
- config-option.ts
- id/id.ts
- cli/ui.ts
- code-mode.ts
- process.ts
- shell/prompt.ts
- acp/session.ts
- workspace-adapter-runtime.ts
- oauth-callback.ts
- xai.ts
- text
- Process
- shared/ui.ts
- native-runtime.ts
- content.ts
- acp/error.ts
- stream.ts
- toolEntryBody
- catalog.ts
- instance-store.ts
- proxy.ts
- auth/index.ts
- uninstall.ts
- mcp/auth.ts
- ws-pool.ts
- provider/error.ts
- webfetch.ts
- export.ts
- span
- groups/sync.ts
- runner.ts
- discovery.ts
- websearch.ts
- acp/event.ts
- env/index.ts
- deriveNewContentsFromChunks
- websocket-tracker.ts
- shell/id.ts
- managed.ts
- profile.ts
- cmd/agent.ts
- browser.ts
- AccountTransportError
- installRoslynLanguageServer
- fileFromDiffPath
- mdns.ts
- bom.ts
- wildcard.ts
- audio.d.ts
- arity.ts
- tool/question.ts
- InitError
- NoProvidersError
- init-projectors.ts
- archive.ts
- markdown.d.ts
- loaded
- sql.d.ts

## God Nodes (most connected - your core abstractions)
1. `RunFooter` - 66 edges
2. `Filesystem` - 50 edges
3. `InstanceState` - 44 edges
4. `SessionID` - 43 edges
5. `reduceSessionData()` - 39 edges
6. `Config` - 39 edges
7. `createLayer()` - 38 edges
8. `Session` - 34 edges
9. `EventV2Bridge` - 31 edges
10. `Provider` - 31 edges

## Surprising Connections (you probably didn't know these)
- `routeHttpApiWorkspace()` --indirect_call--> `plan()`  [INFERRED]
  server/routes/instance/httpapi/middleware/workspace-routing.ts → session/session.ts
- `make()` --indirect_call--> `loaded()`  [INFERRED]
  acp/service.ts → session/instruction.ts
- `make()` --indirect_call--> `messages()`  [INFERRED]
  acp/service.ts → session/llm/native-request.ts
- `make()` --indirect_call--> `model()`  [INFERRED]
  acp/service.ts → session/llm/native-request.ts
- `makeUsageService()` --indirect_call--> `messages()`  [INFERRED]
  acp/service.ts → session/llm/native-request.ts

## Import Cycles
- 3-file cycle: `plugin/index.ts -> session/session.ts -> provider/provider.ts -> plugin/index.ts`
- 3-file cycle: `command/index.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 3-file cycle: `effect/instance-state.ts -> project/instance-context.ts -> project/project.ts -> effect/instance-state.ts`
- 4-file cycle: `plugin/github-copilot/copilot.ts -> session/message-v2.ts -> provider/provider.ts -> plugin/index.ts -> plugin/github-copilot/copilot.ts`
- 4-file cycle: `plugin/index.ts -> session/session.ts -> session/message-v2.ts -> provider/provider.ts -> plugin/index.ts`
- 4-file cycle: `command/index.ts -> config/config.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 4-file cycle: `command/index.ts -> effect/instance-state.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 4-file cycle: `effect/instance-ref.ts -> project/instance-context.ts -> project/project.ts -> effect/instance-state.ts -> effect/instance-ref.ts`
- 4-file cycle: `effect/instance-ref.ts -> project/instance-context.ts -> project/project.ts -> event-v2-bridge.ts -> effect/instance-ref.ts`
- 5-file cycle: `command/index.ts -> config/config.ts -> effect/instance-state.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> effect/bridge.ts -> effect/instance-ref.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> effect/bridge.ts -> effect/run-service.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> effect/instance-state.ts -> effect/instance-ref.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> mcp/index.ts -> config/config.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> mcp/index.ts -> effect/instance-state.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> skill/index.ts -> config/config.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`
- 5-file cycle: `command/index.ts -> skill/index.ts -> effect/instance-state.ts -> project/instance-context.ts -> project/project.ts -> command/index.ts`

## Communities (159 total, 9 thin omitted)

### Community 0 - "session/prompt.ts"
Cohesion: 0.04
Nodes (76): layer, node, Service, PermissionNotFoundError, CommandPayload, DiffQuery, ForkPayload, InitPayload (+68 more)

### Community 1 - "run/types.ts"
Cohesion: 0.06
Nodes (62): cleanRunText(), codeBody(), entryBody(), entryCanStream(), entryDone(), EntryFlags, markdownBody(), reasoningBody() (+54 more)

### Community 2 - "registry.ts"
Cohesion: 0.04
Nodes (67): context, directory, get(), InstanceState, use(), useEffect(), workspaceID, EventV2Bridge (+59 more)

### Community 3 - "run/runtime.ts"
Cohesion: 0.05
Nodes (70): BootService, Config, configTask, defaultRunTuiConfig(), emptyModelInfo(), emptySessionInfo(), layer, loadConfig() (+62 more)

### Community 4 - "app-runtime.ts"
Cohesion: 0.05
Nodes (60): Agent, Command, Default, Event, Info, Interface, layer, node (+52 more)

### Community 5 - "agent/agent.ts"
Cohesion: 0.04
Nodes (56): GeneratedAgent, Info, Interface, layer, locationServiceMapNode, node, TODO: clean this up so provider specific logic doesnt bleed over, Service (+48 more)

### Community 6 - "theme.ts"
Cohesion: 0.06
Nodes (65): createRuntimeLifecycle(), CycleResult, directoryLabel(), Lifecycle, LifecycleInput, queueSplash(), shutdown(), splashInfo() (+57 more)

### Community 7 - "tui/runtime.ts"
Cohesion: 0.07
Nodes (59): TuiConfig, applyPlugin(), errorMessage(), PluginLoader, PluginMeta, readPluginId(), readV1Plugin(), resolvePluginId() (+51 more)

### Community 8 - "transform.ts"
Cohesion: 0.06
Nodes (57): anthropicAdaptiveEfforts(), anthropicEffort(), anthropicOmitsThinking(), anthropicOpus45(), anthropicOpus45Effort(), anthropicUsesModernAdaptiveThinking(), applyCaching(), budgetVariants() (+49 more)

### Community 9 - "provider/provider.ts"
Cohesion: 0.04
Nodes (45): EffectPromise, ModelStatus, ProviderModelStatus, BUNDLED_PROVIDERS, BundledSDK, ConfigProvidersResult, cost(), custom() (+37 more)

### Community 10 - "footer.view.tsx"
Cohesion: 0.07
Nodes (53): categoryRank(), CommandEntry, countLabel(), HALF_BLOCK_BORDER, handleKey(), match(), MenuState, ModelEntry (+45 more)

### Community 11 - "httpapi/server.ts"
Cohesion: 0.05
Nodes (44): BackgroundJob, layer, node, AppNodeBuilderV1, bootstrapReplacement, McpAuth, layer, PluginPtyEnvironment (+36 more)

### Community 12 - "footer.prompt.tsx"
Cohesion: 0.07
Nodes (48): Auto, clamp(), clonePrompt(), createPromptState(), emptyPrompt(), extractLineRange(), Mention, MenuMode (+40 more)

### Community 13 - "RunFooter"
Cohesion: 0.09
Nodes (4): RunFooter, RunFooterOptions, FooterView, createWebSocketFetch()

### Community 14 - "github.handler.ts"
Cohesion: 0.06
Nodes (45): GitHubAuthor, GitHubComment, GitHubCommit, GitHubFile, githubInstall, GitHubIssue, GitHubPullRequest, GitHubReview (+37 more)

### Community 15 - "shared.ts"
Cohesion: 0.08
Nodes (46): error(), deduplicatePluginOrigins(), Origin, pluginSpecifier(), resolvePluginSpec(), attempt(), AttemptResult, Candidate (+38 more)

### Community 16 - "json-schema.ts"
Cohesion: 0.06
Nodes (45): schema, fromRow(), toPublicInfo(), adapterState(), AISDKEvent, copilotTotalNanoAiu(), currentReasoningID(), currentTextID() (+37 more)

### Community 17 - "session-data.ts"
Cohesion: 0.09
Nodes (48): bashCommand(), blockerStatus(), bootstrapSessionData(), claimShell(), Dict, doneShell(), doneTool(), drop() (+40 more)

### Community 18 - "subagent-data.ts"
Cohesion: 0.10
Nodes (47): formatError(), appendCommits(), applyChildEvent(), bootstrapChildEvent(), BootstrapChildMessage, bootstrapChildMessages(), bootstrapSubagentCalls(), bootstrapSubagentData() (+39 more)

### Community 19 - "effect-cmd.ts"
Cohesion: 0.09
Nodes (32): cmd(), WithDoubleDash, AgentCommand, ConfigCommand, FileCommand, FileListCommand, FileReadCommand, FileSearchCommand (+24 more)

### Community 20 - "api.ts"
Cohesion: 0.07
Nodes (32): EventManifest, ProviderAuth, Event, InstanceDisposed, EventSchema, InstanceHttpApiType, RootHttpApi, RootHttpApiType (+24 more)

### Community 21 - "install.ts"
Cohesion: 0.07
Nodes (41): cause(), createPlugTask(), defaultPlugDeps, PlugCtx, PlugDeps, PluginCommand, PlugInput, Spin (+33 more)

### Community 22 - "run/tool.ts"
Cohesion: 0.05
Nodes (20): AnyToolRule, PatchFile, patchTitle(), permWebSearch(), runWebSearch(), scrollWebSearchStart(), snapPatch(), ToolDefs (+12 more)

### Community 23 - "session/session.ts"
Cohesion: 0.05
Nodes (39): ArchivedTimestamp, BusyError, cancelBackgroundJobs, ChildrenInput, CreateInput, EmptyTokens, Event, ForkInput (+31 more)

### Community 24 - "Filesystem"
Cohesion: 0.07
Nodes (33): substituteWellKnownRemoteConfig(), Acc, CurrentWorkingDirectory, resolveHostAttentionSoundPaths(), HostMetadata, Info, Interface, layer (+25 more)

### Community 25 - "lsp/server.ts"
Cohesion: 0.05
Nodes (41): Astro, BashLS, Biome, Clangd, Clojure, CSharp, Dart, Deno (+33 more)

### Community 26 - "demo.ts"
Cohesion: 0.13
Nodes (42): Ask, askPermission(), clearSubagent(), createRunDemo(), doneTool(), emitBash(), emitEdit(), emitError() (+34 more)

### Community 27 - "public.ts"
Cohesion: 0.09
Nodes (40): OpenCodeHttpApi, QueryBoolean, QueryBooleanOpenApi, addLegacyErrorSchemas(), applyLegacySchemaOverrides(), canonicalizeSchema(), canonicalRef(), collapseDuplicateComponents() (+32 more)

### Community 28 - "service.ts"
Cohesion: 0.10
Nodes (39): parseModelSelection(), ACPProfile, AssistantError, AssistantInfo, AuthMethodID, ConfigState, defaultModelFromConfig(), detectSlashCommand() (+31 more)

### Community 29 - "stream.transport.ts"
Cohesion: 0.09
Nodes (40): Deferred, active(), blockerOrder(), composeFooter(), createLayer(), createSessionTransport(), firstByOrder(), formatUnknownError() (+32 more)

### Community 30 - "account/account.ts"
Cohesion: 0.08
Nodes (35): AccountOrgs, ActiveOrg, ClientId, DeviceAuth, DeviceToken, DeviceTokenError, DeviceTokenRequest, DeviceTokenSuccess (+27 more)

### Community 31 - "storage.ts"
Cohesion: 0.06
Nodes (27): pagerCmd(), SessionCommand, SessionDeleteCommand, SessionListCommand, aggregateSessionStats, displayStats(), formatNumber(), getAllSessions (+19 more)

### Community 32 - "message-v2.ts"
Cohesion: 0.06
Nodes (29): DecodeError, Error, Image, Interface, InvalidDataUrlError, JPEG_QUALITIES, layer, node (+21 more)

### Community 33 - "acp/tool.ts"
Cohesion: 0.10
Nodes (37): buildCompletedRawOutput, buildCompletedToolContent, buildCompletedToolUpdate, buildDuplicateRunningToolUpdate, buildErrorToolUpdate, buildPendingToolCall, buildRunningToolUpdate, completedToolContent() (+29 more)

### Community 34 - "compaction.ts"
Cohesion: 0.07
Nodes (31): ProviderTransform, CompletedCompaction, completedCompactions(), Event, layer, node, preserveRecentBudget(), PRUNE_MINIMUM (+23 more)

### Community 35 - "question.shared.ts"
Cohesion: 0.17
Nodes (33): RunQuestionBody(), FOOTER_WIDTH_BREAKPOINTS, footerWidthPolicy(), createQuestionBodyState(), questionAnswers(), QuestionBodyState, questionConfirm(), questionCustom() (+25 more)

### Community 36 - "mcp/index.ts"
Cohesion: 0.06
Nodes (30): AuthResult, AuthStatus, BrowserOpenFailed, createClient(), CreateResult, Failed, Interface, layer (+22 more)

### Community 37 - "errors.ts"
Cohesion: 0.08
Nodes (28): ApiNotFoundError, ConflictError, ForbiddenError, InvalidCursorError, InvalidRequestError, McpServerNotFoundError, MessageNotFoundError, ModelNotFoundError (+20 more)

### Community 38 - "config/config.ts"
Cohesion: 0.07
Nodes (26): Account, Info, Interface, layer, mergeConfig(), mergeConfigConcatArrays(), node, resolveLoadedPlugins() (+18 more)

### Community 39 - "index.ts"
Cohesion: 0.10
Nodes (21): println(), AcpCommand, DbCommand, PathCommand, QueryCommand, DebugCommand, Args, GenerateCommand (+13 more)

### Community 40 - "footer.permission.tsx"
Cohesion: 0.14
Nodes (27): buttons(), RunPermissionBody(), createPermissionBodyState(), data(), Dict, patterns(), permissionAlwaysLines(), PermissionBodyState (+19 more)

### Community 41 - "formatter.ts"
Cohesion: 0.07
Nodes (28): biome, clang, cljfmt, Context, dart, dfmt, gleam, gofmt (+20 more)

### Community 42 - "server/auth.ts"
Cohesion: 0.09
Nodes (22): isActiveOrgChoice(), promptValue(), autocomplete(), log, optional(), password(), select(), text() (+14 more)

### Community 43 - "shell.ts"
Cohesion: 0.09
Nodes (18): ask, auto(), Chunk, CMD_FILES, CWD, envValue(), expand(), FILES (+10 more)

### Community 44 - "tools.ts"
Cohesion: 0.08
Nodes (19): deriveSubagentSessionPermission(), McpCatalog, SessionProcessor, base64Size(), formatBytes(), formatMcpResourceContent(), MCP_RESOURCE_TOOLS, resolve (+11 more)

### Community 45 - "control-plane/workspace.ts"
Cohesion: 0.08
Nodes (25): waitEvent(), ConnectionStatus, CreateError, CreateInput, Event, HistoryEvent, Info, Interface (+17 more)

### Community 46 - "middleware/workspace-routing.ts"
Cohesion: 0.14
Nodes (26): WorkspaceAdapterRuntime, HttpApiProxy, configuredWorkspaceID(), defaultDirectory(), InvalidWorkspaceID, missingWorkspaceResponse(), planRequest(), planWorkspaceRequest() (+18 more)

### Community 47 - "runtime-flags.ts"
Cohesion: 0.08
Nodes (22): emptyConfigLayer, experimental, Info, node, RuntimeFlags, Service, Event, GitResult (+14 more)

### Community 48 - "groups/experimental.ts"
Cohesion: 0.07
Nodes (26): CapabilitiesResponse, ConsoleOrgList, ConsoleOrgOption, ConsoleStateResponse, ConsoleSwitchPayload, ExperimentalApi, ExperimentalPaths, SessionListQuery (+18 more)

### Community 49 - "vcs.ts"
Cohesion: 0.08
Nodes (22): ApplyInput, ApplyResult, batchPatches, diffAgainstRef, DiffOptions, emptyPatch(), Event, FileDiff (+14 more)

### Community 50 - "groups/tui.ts"
Cohesion: 0.10
Nodes (17): CommandPayload, EventTuiCommandExecute, EventTuiPromptAppend, EventTuiSessionSelect, EventTuiToastShow, TuiApi, TuiPaths, TuiPublishPayload (+9 more)

### Community 51 - "acp/permission.ts"
Cohesion: 0.15
Nodes (20): Connection, diffContentForFiles(), diffContentForPatch(), editTitle(), fileMetadata(), Handler, permissionContent(), PermissionEvent (+12 more)

### Community 52 - "worker.ts"
Cohesion: 0.11
Nodes (14): bootstrap(), Heap, rpc, AppRuntime, context, disposeAllInstances(), disposeInstance(), InstanceRuntime (+6 more)

### Community 53 - "markdown.ts"
Cohesion: 0.13
Nodes (19): ConfigAgent, load(), loadMode(), ConfigCommand, decodeInfo, load(), configEntryNameFromPath(), stripPrefix() (+11 more)

### Community 54 - "bridge.ts"
Cohesion: 0.15
Nodes (18): context, WorkspaceContext, wrap(), bind(), captureSync(), fromPromise(), make(), restoreWorkspace() (+10 more)

### Community 55 - "groups/pty.ts"
Cohesion: 0.10
Nodes (21): disposeInstance(), disposers, registerDisposer(), make(), PtyForbiddenError, PtyNotFoundError, CursorQuery, Params (+13 more)

### Community 56 - "middleware/instance-context.ts"
Cohesion: 0.14
Nodes (19): ProjectNotFoundError, QuestionNotFoundError, ConfigApi, EventPaths, PermissionApi, ReplyPayload, GenerateNamePayload, ProjectCopyApi (+11 more)

### Community 57 - "usage.ts"
Cohesion: 0.09
Nodes (19): AssistantMessage, AssistantTokenCost, ContextLimitLoader, ContextLimitLoaderInterface, contextLimitLoaderLayer, contextLimitLoaderNode, Interface, layer (+11 more)

### Community 58 - "run.ts"
Cohesion: 0.11
Nodes (18): block(), FilePart, formatRunError(), MiniCommandInput, ModelInput, RunCommand, INTERACTIVE_INPUT_ERROR, InteractiveStdin (+10 more)

### Community 59 - "installation/index.ts"
Cohesion: 0.08
Nodes (17): BrewFormula, BrewInfoV2, ChocoPackage, Event, GitHubRelease, Info, Interface, layer (+9 more)

### Community 60 - "client.ts"
Cohesion: 0.11
Nodes (20): CapabilityRegistration, configurationValue(), create(), dedupeDiagnostics(), Diagnostic, DiagnosticRequestResult, DocumentDiagnosticReport, getFilePath() (+12 more)

### Community 61 - "patch/index.ts"
Cohesion: 0.10
Nodes (24): AffectedPaths, applyHunksToFiles, applyPatch, ApplyPatchAction, ApplyPatchArgs, ApplyPatchError, ApplyPatchFileChange, ApplyPatchFileUpdate (+16 more)

### Community 62 - "server/server.ts"
Cohesion: 0.12
Nodes (21): Scope, disposeMiddleware(), PublicApi, HttpApiApp, Default, EffectListener, forceClose(), listen() (+13 more)

### Community 63 - "question/index.ts"
Cohesion: 0.11
Nodes (20): Answer, Event, Info, Interface, layer, node, NotFoundError, PendingEntry (+12 more)

### Community 64 - "McpOAuthProvider"
Cohesion: 0.09
Nodes (4): McpOAuthCallbacks, McpOAuthConfig, McpOAuthPendingProvider, McpOAuthProvider

### Community 65 - "provider/auth.ts"
Cohesion: 0.09
Nodes (22): Authorization, AuthorizeInput, CallbackInput, Error, Hook, Interface, layer, Method (+14 more)

### Community 66 - "skill/index.ts"
Cohesion: 0.09
Nodes (19): Discovery, add, discoverSkills, DiscoveryState, fmt(), Info, Interface, InvalidError (+11 more)

### Community 67 - "filesystem.ts"
Cohesion: 0.13
Nodes (13): exists(), findUp(), isEnoent(), normalizePath(), normalizePathPattern(), resolve(), size(), stat() (+5 more)

### Community 69 - "handlers/global.ts"
Cohesion: 0.16
Nodes (15): GlobalBus, GlobalEvent, upgrade(), Installation, disposeAllInstancesAndEmitGlobalDisposed, emitGlobalDisposed, GlobalLifecycle, EventApi (+7 more)

### Community 70 - "retry.ts"
Cohesion: 0.13
Nodes (19): parseToolParams(), cap(), delay(), Err, GO_UPSELL_MESSAGE, GO_UPSELL_URL, matchesRetryableMessage(), num() (+11 more)

### Community 71 - "providers.ts"
Cohesion: 0.09
Nodes (14): decodeMessageInfo, decodePart, ExportData, ImportCommand, runImport, ShareData, handlePluginAuth, PluginAuth (+6 more)

### Community 72 - "digitalocean.ts"
Cohesion: 0.10
Nodes (12): buildAuthorizeUrl(), ImplicitTokenPayload, PendingOAuth, redirectUri(), RouterEntry, ModalPlugin(), decode, get() (+4 more)

### Community 73 - "meta.ts"
Cohesion: 0.16
Nodes (21): Core, Entry, entryCore(), fileTarget(), fingerprint(), list(), lock(), modifiedAt() (+13 more)

### Community 74 - "cmd/mcp.ts"
Cohesion: 0.12
Nodes (18): addMcpToConfig(), authState(), configuredServers(), isMcpConfigured(), isMcpRemote(), listState(), McpAddCommand, McpAuthCommand (+10 more)

### Community 75 - "ws.ts"
Cohesion: 0.13
Nodes (13): abortError(), cancelError(), connectResponsesWebSocket(), ConnectResponsesWebSocketOptions, isAbortError(), PROTOCOL_HEADER, StreamResponsesWebSocketOptions, WrappedError (+5 more)

### Community 76 - "groups/workspace.ts"
Cohesion: 0.12
Nodes (13): Workspace, ApiVcsApplyError, ApiWorkspaceCreateError, ApiWorkspaceWarpError, CreatePayload, WarpPayload, WorkspaceApi, WorkspacePaths (+5 more)

### Community 77 - "plugin/index.ts"
Cohesion: 0.15
Nodes (18): AzureAuthPlugin(), CloudflareAIGatewayAuthPlugin(), CloudflareWorkersAuthPlugin(), DigitalOceanAuthPlugin(), CopilotAuthPlugin(), experimentalWebSocketsEnabled(), getLegacyPlugins(), getServerPlugin() (+10 more)

### Community 78 - "codex.ts"
Cohesion: 0.15
Nodes (19): ALLOWED_MODELS, base64UrlEncode(), buildAuthorizeUrl(), CodexAuthPlugin(), CodexAuthPluginOptions, DISALLOWED_MODELS, exchangeCodeForTokens(), extractAccountId() (+11 more)

### Community 79 - "message.ts"
Cohesion: 0.11
Nodes (19): ProviderError, AuthError, MessageError, OutputLengthError, Shared, SharedSchema, FilePart, Info (+11 more)

### Community 80 - "edit.ts"
Cohesion: 0.15
Nodes (16): BlockAnchorReplacer(), ContextAwareReplacer(), EditTool, EscapeNormalizedReplacer(), IndentationFlexibleReplacer(), isDisproportionateMatch(), levenshtein(), LineTrimmedReplacer() (+8 more)

### Community 81 - "worktree/index.ts"
Cohesion: 0.10
Nodes (19): CreateFailedError, CreateInput, Error, Event, GitResult, Info, Interface, layer (+11 more)

### Community 82 - "toolPath"
Cohesion: 0.12
Nodes (20): count(), info(), lspTitle(), permEdit(), permLsp(), permRead(), runEdit(), runGlob() (+12 more)

### Community 83 - "adapters/index.ts"
Cohesion: 0.15
Nodes (17): BUILTIN, listAdapters(), registerAdapter(), registeredAdapters(), state, decodeWorktreeConfig, loadWorktree(), provideContext() (+9 more)

### Community 84 - "authorization.ts"
Cohesion: 0.14
Nodes (15): ServerAuth, authorizationLayer, authorizationRouterMiddleware, credentialFromRequest(), credentialFromURL(), decodeCredential(), emptyCredential(), ptyConnectAuthorizationLayer (+7 more)

### Community 85 - "Agent"
Cohesion: 0.18
Nodes (3): ACP, Agent, run()

### Community 86 - "snowflake-cortex.ts"
Cohesion: 0.17
Nodes (17): OAUTH_DUMMY_KEY, authBasicHeader(), authHeaders(), base64UrlEncode(), buildAuthorizeUrl(), callbackUrl(), exchangeCodeForToken(), generatePKCE() (+9 more)

### Community 87 - "cmd/account.ts"
Cohesion: 0.13
Nodes (17): activeSuffix(), ConsoleCommand, defaultConsoleUrl, dim(), formatAccountLabel(), formatOrgChoiceLabel(), formatOrgLine(), LoginCommand (+9 more)

### Community 88 - "copilot.ts"
Cohesion: 0.14
Nodes (14): base(), normalizeDomain(), RFC-8628, UTILITY_MODELS, build(), CopilotEndpoint, CopilotModel, CopilotModels (+6 more)

### Community 89 - "native-request.ts"
Cohesion: 0.20
Nodes (18): baseURL(), content(), contentPart(), generation(), mediaPart(), messages(), model(), partProviderMetadata() (+10 more)

### Community 90 - "directory.ts"
Cohesion: 0.12
Nodes (17): build(), DefaultModel, Directory, Interface, layer, Loader, LoaderInterface, loaderLayer (+9 more)

### Community 91 - "session-replay.ts"
Cohesion: 0.17
Nodes (17): createSessionData(), SessionData, active(), apply(), isShellSyntheticAssistant(), isShellSyntheticUser(), mergePatch(), replayActiveText() (+9 more)

### Community 92 - "cmd/tui.ts"
Cohesion: 0.18
Nodes (14): createEventSource(), createWorkerFetch(), resolveThreadDirectory(), RpcClient, target(), TuiThreadCommand, hasArg(), hasBooleanArg() (+6 more)

### Community 93 - "git/index.ts"
Cohesion: 0.12
Nodes (13): Base, cfg, Interface, Item, Kind, layer, node, Options (+5 more)

### Community 94 - "truncate.ts"
Cohesion: 0.14
Nodes (14): evaluate(), DIR, hasTaskTool(), Interface, layer, MAX_BYTES, MAX_LINES, node (+6 more)

### Community 95 - "repo.ts"
Cohesion: 0.18
Nodes (14): AccountRepo, AccountRow, Interface, layer, node, Service, use, AccountID (+6 more)

### Community 96 - "config-option.ts"
Cohesion: 0.22
Nodes (15): buildConfigOptions(), buildEffortSelectOption(), buildModelSelectOption(), buildModelSelectOptions(), buildModeSelectOption(), ConfigOptionMode, ConfigOptionModel, ConfigOptionProvider (+7 more)

### Community 97 - "id/id.ts"
Cohesion: 0.17
Nodes (11): GlobalBusEmitter, ascending(), create(), descending(), generateID(), Identifier, prefixes, randomBase62() (+3 more)

### Community 98 - "cli/ui.ts"
Cohesion: 0.15
Nodes (8): AttachCommand, decodeSessionID, validateSession(), CancelledError, empty(), println(), Style, wordmark

### Community 99 - "code-mode.ts"
Cohesion: 0.16
Nodes (15): Attachment, CallEntry, CatalogEntry, CODE_MODE_TOOL, CodeModeTool, dataUrl(), describeCatalog(), groupByServer() (+7 more)

### Community 100 - "process.ts"
Cohesion: 0.17
Nodes (14): cmd(), Child, lines(), Options, Result, run(), RunFailedError, RunOptions (+6 more)

### Community 101 - "shell/prompt.ts"
Cohesion: 0.23
Nodes (15): bashCommandSection(), chainGuidance(), CMD, cmdCommandSection(), Limits, Parameters, parameterSchema(), powershellCommandSection() (+7 more)

### Community 102 - "acp/session.ts"
Cohesion: 0.13
Nodes (12): Info, Interface, KnownMessagePartMetadata, layer, node, PartMetadataLookupInput, RecordPartMetadataInput, SelectedModel (+4 more)

### Community 103 - "workspace-adapter-runtime.ts"
Cohesion: 0.23
Nodes (13): getAdapter(), configure(), context, create(), list(), remove(), target(), EffectBridge (+5 more)

### Community 104 - "oauth-callback.ts"
Cohesion: 0.21
Nodes (13): cancelPending(), cleanupStateIndex(), ensureRunning(), handleRequest(), isPortInUse(), mcpNameToState, McpOAuthCallback, PendingAuth (+5 more)

### Community 105 - "xai.ts"
Cohesion: 0.19
Nodes (12): authHeaders(), DeviceCodeResponse, DeviceTokenErrorBody, pollDeviceCodeToken(), positiveSecondsToMs(), refreshAccessToken(), RefreshResult, requestDeviceCode() (+4 more)

### Community 106 - "text"
Cohesion: 0.15
Nodes (14): fallbackInline(), frame(), permList(), runBash(), runBatch(), runInvalid(), runList(), runPlanExit() (+6 more)

### Community 107 - "Process"
Cohesion: 0.18
Nodes (11): AlreadyInstalledError, Event, Ide, install(), InstallFailedError, SUPPORTED_IDES, Child, spawn() (+3 more)

### Community 108 - "shared/ui.ts"
Cohesion: 0.27
Nodes (13): csp(), cspForHtml(), DEFAULT_CSP, embeddedUI(), embeddedUIResponse(), notFound(), proxyResponseHeaders(), requestBody() (+5 more)

### Community 109 - "native-runtime.ts"
Cohesion: 0.23
Nodes (12): LLMNative, LLMNativeRuntime, nativeSchema(), nativeTools(), providerFetch(), providerHeaders(), RuntimeStatus, status() (+4 more)

### Community 110 - "content.ts"
Cohesion: 0.28
Nodes (12): audienceFlags(), contentBlockToParts(), decodeDataUrl(), filenameFromUri(), filePartToContentChunks(), partAudience(), partsToContentChunks(), partToContentChunks() (+4 more)

### Community 111 - "acp/error.ts"
Cohesion: 0.15
Nodes (10): AuthRequiredError, Error, InvalidConfigOptionError, InvalidEffortError, InvalidModeError, InvalidModelError, ServiceFailureError, SessionNotFoundError (+2 more)

### Community 112 - "stream.ts"
Cohesion: 0.23
Nodes (11): OutputInput, patch(), StreamOutput, summarize(), Trace, traceCommit(), traceFooterOutput(), traceSubagentState() (+3 more)

### Community 113 - "toolEntryBody"
Cohesion: 0.18
Nodes (13): fallbackFinal(), fallbackStart(), key(), markdownBody(), props(), rule(), shellOutput(), structuredBody() (+5 more)

### Community 114 - "catalog.ts"
Cohesion: 0.26
Nodes (11): defs(), fetch(), isOutputSchemaValidationError(), listTools(), paginate(), prompts(), resources(), resourceTemplates() (+3 more)

### Community 115 - "instance-store.ts"
Cohesion: 0.19
Nodes (11): InstanceBootstrap, Interface, Service, InstanceContext, bootstrapNode, Entry, Interface, layer (+3 more)

### Community 116 - "proxy.ts"
Cohesion: 0.26
Nodes (9): headers(), hop, ProxyUtil, sanitize(), http(), requestBody(), statusText(), websocket() (+1 more)

### Community 117 - "auth/index.ts"
Cohesion: 0.17
Nodes (10): Api, AuthError, file, Info, Interface, layer, node, Oauth (+2 more)

### Community 118 - "uninstall.ts"
Cohesion: 0.24
Nodes (11): cleanShellConfig(), collectRemovalTargets(), executeUninstall(), formatSize(), getDirectorySize(), getShellConfigFile(), RemovalTargets, shortenPath() (+3 more)

### Community 119 - "mcp/auth.ts"
Cohesion: 0.17
Nodes (11): AuthData, ClientInfo, decodeAuthData, Entry, filepath, Interface, layer, node (+3 more)

### Community 120 - "ws-pool.ts"
Cohesion: 0.20
Nodes (7): OpenAIWebSocket, CreateWebSocketFetchOptions, invalidate(), OpenAIWebSocketPool, PoolEntry, socket(), TITLE_HEADER

### Community 121 - "provider/error.ts"
Cohesion: 0.23
Nodes (9): HeaderTimeoutError, isOpenAiErrorRetryable(), json(), message(), parseAPICallError(), ParsedAPICallError, ParsedStreamError, parseStreamError() (+1 more)

### Community 122 - "webfetch.ts"
Cohesion: 0.24
Nodes (9): parser, extractTextFromHTML(), Parameters, WebFetchTool, isImageAttachment(), isMedia(), isPdfAttachment(), sniffAttachmentMime() (+1 more)

### Community 123 - "export.ts"
Cohesion: 0.38
Nodes (10): data(), diff(), ExportCommand, filepart(), part(), redact(), run, sanitize() (+2 more)

### Community 124 - "span"
Cohesion: 0.22
Nodes (11): fail(), num(), patchLine(), scrollBashFinal(), scrollGlobFinal(), scrollPatchFinal(), scrollQuestionFinal(), scrollTaskFinal() (+3 more)

### Community 125 - "groups/sync.ts"
Cohesion: 0.24
Nodes (9): HistoryEvent, HistoryPayload, ReplayEvent, ReplayPayload, ReplayResponse, SessionPayload, SyncApi, SyncPaths (+1 more)

### Community 126 - "runner.ts"
Cohesion: 0.20
Nodes (9): shell(), Busy, Cancelled, make(), PendingHandle, RunHandle, Runner, ShellHandle (+1 more)

### Community 127 - "discovery.ts"
Cohesion: 0.25
Nodes (7): Index, IndexSkill, Interface, layer, node, Service, withTransientReadRetry()

### Community 128 - "websearch.ts"
Cohesion: 0.28
Nodes (7): callProvider(), parallelAuthHeaders(), Parameters, webSearchModelName(), WebSearchProvider, WebSearchProviderSchema, WebSearchTool

### Community 129 - "acp/event.ts"
Cohesion: 0.25
Nodes (7): ReplayPart, ACPEvent, Connection, GlobalEventEnvelope, GlobalEventStream, start(), ACPPermission

### Community 130 - "env/index.ts"
Cohesion: 0.25
Nodes (7): Env, Interface, layer, node, Service, State, use

### Community 131 - "deriveNewContentsFromChunks"
Cohesion: 0.25
Nodes (8): applyReplacements(), computeReplacements(), deriveNewContentsFromChunks(), generateUnifiedDiff(), normalizeUnicode(), seekSequence(), tryMatch(), BOM

### Community 132 - "websocket-tracker.ts"
Cohesion: 0.25
Nodes (6): Close, Interface, layer, node, register(), Service

### Community 133 - "shell/id.ts"
Cohesion: 0.29
Nodes (7): isKind(), Kind, kinds, ShellID, shellKinds, toKind(), ToolID

### Community 134 - "managed.ts"
Cohesion: 0.43
Nodes (6): ConfigManaged, managedConfigDir(), parseManagedPlist(), PLIST_META, readManagedPreferences(), systemManagedConfigDir()

### Community 135 - "profile.ts"
Cohesion: 0.53
Nodes (5): duration(), mark(), measure(), started, write()

### Community 136 - "cmd/agent.ts"
Cohesion: 0.33
Nodes (5): AgentCommand, AgentCreateCommand, AgentListCommand, AgentMode, AVAILABLE_PERMISSIONS

### Community 137 - "browser.ts"
Cohesion: 0.33
Nodes (5): Interface, layer, McpBrowser, node, Service

### Community 138 - "AccountTransportError"
Cohesion: 0.40
Nodes (3): accountErrorFromCause(), mapAccountServiceError(), AccountTransportError

### Community 139 - "installRoslynLanguageServer"
Cohesion: 0.50
Nodes (5): findVscodeRazorExtension(), getRoslynLanguageServer(), installRoslynLanguageServer(), pathExists(), roslynLanguageServerGlobalPath()

### Community 140 - "fileFromDiffPath"
Cohesion: 0.60
Nodes (5): fileFromDiffPath(), fileFromGitHeader(), fileFromPatchChunk(), parsePathToken(), parseQuotedPath()

### Community 141 - "mdns.ts"
Cohesion: 0.60
Nodes (4): MDNS, publish(), unpublish(), setupMdns()

### Community 142 - "bom.ts"
Cohesion: 0.50
Nodes (4): join(), readFile, split(), syncFile

### Community 143 - "wildcard.ts"
Cohesion: 0.80
Nodes (4): all(), allStructured(), match(), matchSequence()

### Community 144 - "audio.d.ts"
Cohesion: 0.50
Nodes (3): *.mp3, *.wasm, *.wav

### Community 147 - "tool/question.ts"
Cohesion: 0.50
Nodes (3): Metadata, Parameters, QuestionTool

## Knowledge Gaps
- **1355 isolated node(s):** `AccountOrgs`, `ActiveOrg`, `RemoteConfig`, `DurationFromSeconds`, `TokenRefresh` (+1350 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **9 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Session` connect `session/prompt.ts` to `registry.ts`, `app-runtime.ts`, `agent/agent.ts`, `theme.ts`, `httpapi/server.ts`, `github.handler.ts`, `session/session.ts`, `storage.ts`, `compaction.ts`, `config/config.ts`, `tools.ts`, `control-plane/workspace.ts`, `middleware/workspace-routing.ts`, `runtime-flags.ts`, `groups/experimental.ts`, `groups/tui.ts`, `providers.ts`, `plugin/index.ts`, `code-mode.ts`, `export.ts`, `groups/sync.ts`?**
  _High betweenness centrality (0.027) - this node is a cross-community bridge._
- **Why does `RuntimeFlags` connect `runtime-flags.ts` to `session/prompt.ts`, `websearch.ts`, `compaction.ts`, `registry.ts`, `app-runtime.ts`, `agent/agent.ts`, `skill/index.ts`, `tui/runtime.ts`, `provider/provider.ts`, `httpapi/server.ts`, `tools.ts`, `plugin/index.ts`, `control-plane/workspace.ts`, `shell.ts`, `session/session.ts`, `lsp/server.ts`?**
  _High betweenness centrality (0.025) - this node is a cross-community bridge._
- **Why does `SessionID` connect `session/prompt.ts` to `registry.ts`, `agent/agent.ts`, `httpapi/server.ts`, `github.handler.ts`, `session/session.ts`, `storage.ts`, `message-v2.ts`, `compaction.ts`, `config/config.ts`, `tools.ts`, `control-plane/workspace.ts`, `middleware/workspace-routing.ts`, `runtime-flags.ts`, `groups/experimental.ts`, `question/index.ts`, `message.ts`, `cli/ui.ts`, `export.ts`, `groups/sync.ts`?**
  _High betweenness centrality (0.022) - this node is a cross-community bridge._
- **What connects `AccountOrgs`, `ActiveOrg`, `RemoteConfig` to the rest of the system?**
  _1355 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `session/prompt.ts` be split into smaller, more focused modules?**
  _Cohesion score 0.04276315789473684 - nodes in this community are weakly interconnected._
- **Should `run/types.ts` be split into smaller, more focused modules?**
  _Cohesion score 0.057729138166894664 - nodes in this community are weakly interconnected._
- **Should `registry.ts` be split into smaller, more focused modules?**
  _Cohesion score 0.04005602240896359 - nodes in this community are weakly interconnected._