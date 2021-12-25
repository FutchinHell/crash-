# crash-
net.fabricmc.loader.impl.FormattedException: java.lang.RuntimeException: Could not execute entrypoint stage 'preLaunch' due to errors, provided by 'advanced_runtime_resource_pack'!
	at net.fabricmc.loader.impl.launch.knot.Knot.init(Knot.java:159)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:71)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
Caused by: java.lang.RuntimeException: Could not execute entrypoint stage 'preLaunch' due to errors, provided by 'advanced_runtime_resource_pack'!
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.lambda$invoke0$0(EntrypointUtils.java:51)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:49)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke(EntrypointUtils.java:35)
	at net.fabricmc.loader.impl.launch.knot.Knot.init(Knot.java:157)
	... 2 more
Caused by: net.fabricmc.loader.api.EntrypointException: Exception while loading entries for entrypoint 'preLaunch' provided by 'advanced_runtime_resource_pack'
	at net.fabricmc.loader.impl.entrypoint.EntrypointContainerImpl.getEntrypoint(EntrypointContainerImpl.java:56)
	at net.fabricmc.loader.impl.entrypoint.EntrypointUtils.invoke0(EntrypointUtils.java:47)
	... 4 more
Caused by: java.lang.RuntimeException: Mixin transformation of net.devtech.arrp.ARRP failed
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:252)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.tryLoadClass(KnotClassDelegate.java:150)
	at net.fabricmc.loader.impl.launch.knot.KnotClassLoader.loadClass(KnotClassLoader.java:155)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:520)
	at java.base/java.lang.Class.forName0(Native Method)
	at java.base/java.lang.Class.forName(Class.java:467)
	at net.fabricmc.loader.impl.util.DefaultLanguageAdapter.create(DefaultLanguageAdapter.java:50)
	at net.fabricmc.loader.impl.entrypoint.EntrypointStorage$NewEntry.getOrCreate(EntrypointStorage.java:117)
	at net.fabricmc.loader.impl.entrypoint.EntrypointContainerImpl.getEntrypoint(EntrypointContainerImpl.java:53)
	... 5 more
Caused by: org.spongepowered.asm.mixin.throwables.MixinApplyError: Mixin [mixins.mm.json:net.minecraft.class_2960] from phase [DEFAULT] in config [mixins.mm.json] from mod [mm] FAILED during PREPARE
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.handleMixinError(MixinProcessor.java:638)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.handleMixinPrepareError(MixinProcessor.java:585)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.prepareConfigs(MixinProcessor.java:570)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.select(MixinProcessor.java:462)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.checkSelect(MixinProcessor.java:438)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:290)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClass(MixinTransformer.java:234)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClassBytes(MixinTransformer.java:202)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:247)
	... 13 more
Caused by: org.spongepowered.asm.mixin.transformer.throwables.MixinTargetAlreadyLoadedException: Critical problem: mixins.mm.json:net.minecraft.class_2960 target net.minecraft.class_2960 was loaded too early.
	at org.spongepowered.asm.mixin.transformer.MixinInfo.readDeclaredTargets(MixinInfo.java:948)
	at org.spongepowered.asm.mixin.transformer.MixinInfo.<init>(MixinInfo.java:882)
	at org.spongepowered.asm.mixin.transformer.MixinConfig.prepareMixins(MixinConfig.java:852)
	at org.spongepowered.asm.mixin.transformer.MixinConfig.postInitialise(MixinConfig.java:797)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.prepareConfigs(MixinProcessor.java:568)
	... 19 more
