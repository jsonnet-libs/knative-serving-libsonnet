---
permalink: /1.16.0/serving/v1/revision/
---

# serving.v1.revision

"Revision is an immutable snapshot of code and configuration.  A revision\nreferences a container image. Revisions are created by updates to a\nConfiguration.\n\n\nSee also: https://github.com/knative/serving/blob/main/docs/spec/overview.md#revision"

## Index

* [`fn new(name)`](#fn-new)
* [`obj metadata`](#obj-metadata)
  * [`fn withAnnotations(annotations)`](#fn-metadatawithannotations)
  * [`fn withAnnotationsMixin(annotations)`](#fn-metadatawithannotationsmixin)
  * [`fn withClusterName(clusterName)`](#fn-metadatawithclustername)
  * [`fn withCreationTimestamp(creationTimestamp)`](#fn-metadatawithcreationtimestamp)
  * [`fn withDeletionGracePeriodSeconds(deletionGracePeriodSeconds)`](#fn-metadatawithdeletiongraceperiodseconds)
  * [`fn withDeletionTimestamp(deletionTimestamp)`](#fn-metadatawithdeletiontimestamp)
  * [`fn withFinalizers(finalizers)`](#fn-metadatawithfinalizers)
  * [`fn withFinalizersMixin(finalizers)`](#fn-metadatawithfinalizersmixin)
  * [`fn withGenerateName(generateName)`](#fn-metadatawithgeneratename)
  * [`fn withGeneration(generation)`](#fn-metadatawithgeneration)
  * [`fn withLabels(labels)`](#fn-metadatawithlabels)
  * [`fn withLabelsMixin(labels)`](#fn-metadatawithlabelsmixin)
  * [`fn withName(name)`](#fn-metadatawithname)
  * [`fn withNamespace(namespace)`](#fn-metadatawithnamespace)
  * [`fn withOwnerReferences(ownerReferences)`](#fn-metadatawithownerreferences)
  * [`fn withOwnerReferencesMixin(ownerReferences)`](#fn-metadatawithownerreferencesmixin)
  * [`fn withResourceVersion(resourceVersion)`](#fn-metadatawithresourceversion)
  * [`fn withSelfLink(selfLink)`](#fn-metadatawithselflink)
  * [`fn withUid(uid)`](#fn-metadatawithuid)
* [`obj spec`](#obj-spec)
  * [`fn withAffinity(affinity)`](#fn-specwithaffinity)
  * [`fn withAffinityMixin(affinity)`](#fn-specwithaffinitymixin)
  * [`fn withAutomountServiceAccountToken(automountServiceAccountToken)`](#fn-specwithautomountserviceaccounttoken)
  * [`fn withContainerConcurrency(containerConcurrency)`](#fn-specwithcontainerconcurrency)
  * [`fn withContainers(containers)`](#fn-specwithcontainers)
  * [`fn withContainersMixin(containers)`](#fn-specwithcontainersmixin)
  * [`fn withDnsConfig(dnsConfig)`](#fn-specwithdnsconfig)
  * [`fn withDnsConfigMixin(dnsConfig)`](#fn-specwithdnsconfigmixin)
  * [`fn withDnsPolicy(dnsPolicy)`](#fn-specwithdnspolicy)
  * [`fn withEnableServiceLinks(enableServiceLinks)`](#fn-specwithenableservicelinks)
  * [`fn withHostAliases(hostAliases)`](#fn-specwithhostaliases)
  * [`fn withHostAliasesMixin(hostAliases)`](#fn-specwithhostaliasesmixin)
  * [`fn withHostIPC(hostIPC)`](#fn-specwithhostipc)
  * [`fn withHostNetwork(hostNetwork)`](#fn-specwithhostnetwork)
  * [`fn withHostPID(hostPID)`](#fn-specwithhostpid)
  * [`fn withIdleTimeoutSeconds(idleTimeoutSeconds)`](#fn-specwithidletimeoutseconds)
  * [`fn withImagePullSecrets(imagePullSecrets)`](#fn-specwithimagepullsecrets)
  * [`fn withImagePullSecretsMixin(imagePullSecrets)`](#fn-specwithimagepullsecretsmixin)
  * [`fn withInitContainers(initContainers)`](#fn-specwithinitcontainers)
  * [`fn withInitContainersMixin(initContainers)`](#fn-specwithinitcontainersmixin)
  * [`fn withNodeSelector(nodeSelector)`](#fn-specwithnodeselector)
  * [`fn withNodeSelectorMixin(nodeSelector)`](#fn-specwithnodeselectormixin)
  * [`fn withPriorityClassName(priorityClassName)`](#fn-specwithpriorityclassname)
  * [`fn withResponseStartTimeoutSeconds(responseStartTimeoutSeconds)`](#fn-specwithresponsestarttimeoutseconds)
  * [`fn withRuntimeClassName(runtimeClassName)`](#fn-specwithruntimeclassname)
  * [`fn withSchedulerName(schedulerName)`](#fn-specwithschedulername)
  * [`fn withSecurityContext(securityContext)`](#fn-specwithsecuritycontext)
  * [`fn withSecurityContextMixin(securityContext)`](#fn-specwithsecuritycontextmixin)
  * [`fn withServiceAccountName(serviceAccountName)`](#fn-specwithserviceaccountname)
  * [`fn withShareProcessNamespace(shareProcessNamespace)`](#fn-specwithshareprocessnamespace)
  * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-specwithtimeoutseconds)
  * [`fn withTolerations(tolerations)`](#fn-specwithtolerations)
  * [`fn withTolerationsMixin(tolerations)`](#fn-specwithtolerationsmixin)
  * [`fn withTopologySpreadConstraints(topologySpreadConstraints)`](#fn-specwithtopologyspreadconstraints)
  * [`fn withTopologySpreadConstraintsMixin(topologySpreadConstraints)`](#fn-specwithtopologyspreadconstraintsmixin)
  * [`fn withVolumes(volumes)`](#fn-specwithvolumes)
  * [`fn withVolumesMixin(volumes)`](#fn-specwithvolumesmixin)
  * [`obj spec.containers`](#obj-speccontainers)
    * [`fn withArgs(args)`](#fn-speccontainerswithargs)
    * [`fn withArgsMixin(args)`](#fn-speccontainerswithargsmixin)
    * [`fn withCommand(command)`](#fn-speccontainerswithcommand)
    * [`fn withCommandMixin(command)`](#fn-speccontainerswithcommandmixin)
    * [`fn withEnv(env)`](#fn-speccontainerswithenv)
    * [`fn withEnvFrom(envFrom)`](#fn-speccontainerswithenvfrom)
    * [`fn withEnvFromMixin(envFrom)`](#fn-speccontainerswithenvfrommixin)
    * [`fn withEnvMixin(env)`](#fn-speccontainerswithenvmixin)
    * [`fn withImage(image)`](#fn-speccontainerswithimage)
    * [`fn withImagePullPolicy(imagePullPolicy)`](#fn-speccontainerswithimagepullpolicy)
    * [`fn withName(name)`](#fn-speccontainerswithname)
    * [`fn withPorts(ports)`](#fn-speccontainerswithports)
    * [`fn withPortsMixin(ports)`](#fn-speccontainerswithportsmixin)
    * [`fn withTerminationMessagePath(terminationMessagePath)`](#fn-speccontainerswithterminationmessagepath)
    * [`fn withTerminationMessagePolicy(terminationMessagePolicy)`](#fn-speccontainerswithterminationmessagepolicy)
    * [`fn withVolumeMounts(volumeMounts)`](#fn-speccontainerswithvolumemounts)
    * [`fn withVolumeMountsMixin(volumeMounts)`](#fn-speccontainerswithvolumemountsmixin)
    * [`fn withWorkingDir(workingDir)`](#fn-speccontainerswithworkingdir)
    * [`obj spec.containers.env`](#obj-speccontainersenv)
      * [`fn withName(name)`](#fn-speccontainersenvwithname)
      * [`fn withValue(value)`](#fn-speccontainersenvwithvalue)
      * [`obj spec.containers.env.valueFrom`](#obj-speccontainersenvvaluefrom)
        * [`fn withFieldRef(fieldRef)`](#fn-speccontainersenvvaluefromwithfieldref)
        * [`fn withFieldRefMixin(fieldRef)`](#fn-speccontainersenvvaluefromwithfieldrefmixin)
        * [`fn withResourceFieldRef(resourceFieldRef)`](#fn-speccontainersenvvaluefromwithresourcefieldref)
        * [`fn withResourceFieldRefMixin(resourceFieldRef)`](#fn-speccontainersenvvaluefromwithresourcefieldrefmixin)
        * [`obj spec.containers.env.valueFrom.configMapKeyRef`](#obj-speccontainersenvvaluefromconfigmapkeyref)
          * [`fn withKey(key)`](#fn-speccontainersenvvaluefromconfigmapkeyrefwithkey)
          * [`fn withName(name)`](#fn-speccontainersenvvaluefromconfigmapkeyrefwithname)
          * [`fn withOptional(optional)`](#fn-speccontainersenvvaluefromconfigmapkeyrefwithoptional)
        * [`obj spec.containers.env.valueFrom.secretKeyRef`](#obj-speccontainersenvvaluefromsecretkeyref)
          * [`fn withKey(key)`](#fn-speccontainersenvvaluefromsecretkeyrefwithkey)
          * [`fn withName(name)`](#fn-speccontainersenvvaluefromsecretkeyrefwithname)
          * [`fn withOptional(optional)`](#fn-speccontainersenvvaluefromsecretkeyrefwithoptional)
    * [`obj spec.containers.envFrom`](#obj-speccontainersenvfrom)
      * [`fn withPrefix(prefix)`](#fn-speccontainersenvfromwithprefix)
      * [`obj spec.containers.envFrom.configMapRef`](#obj-speccontainersenvfromconfigmapref)
        * [`fn withName(name)`](#fn-speccontainersenvfromconfigmaprefwithname)
        * [`fn withOptional(optional)`](#fn-speccontainersenvfromconfigmaprefwithoptional)
      * [`obj spec.containers.envFrom.secretRef`](#obj-speccontainersenvfromsecretref)
        * [`fn withName(name)`](#fn-speccontainersenvfromsecretrefwithname)
        * [`fn withOptional(optional)`](#fn-speccontainersenvfromsecretrefwithoptional)
    * [`obj spec.containers.livenessProbe`](#obj-speccontainerslivenessprobe)
      * [`fn withFailureThreshold(failureThreshold)`](#fn-speccontainerslivenessprobewithfailurethreshold)
      * [`fn withInitialDelaySeconds(initialDelaySeconds)`](#fn-speccontainerslivenessprobewithinitialdelayseconds)
      * [`fn withPeriodSeconds(periodSeconds)`](#fn-speccontainerslivenessprobewithperiodseconds)
      * [`fn withSuccessThreshold(successThreshold)`](#fn-speccontainerslivenessprobewithsuccessthreshold)
      * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-speccontainerslivenessprobewithtimeoutseconds)
      * [`obj spec.containers.livenessProbe.exec`](#obj-speccontainerslivenessprobeexec)
        * [`fn withCommand(command)`](#fn-speccontainerslivenessprobeexecwithcommand)
        * [`fn withCommandMixin(command)`](#fn-speccontainerslivenessprobeexecwithcommandmixin)
      * [`obj spec.containers.livenessProbe.grpc`](#obj-speccontainerslivenessprobegrpc)
        * [`fn withPort(port)`](#fn-speccontainerslivenessprobegrpcwithport)
        * [`fn withService(service)`](#fn-speccontainerslivenessprobegrpcwithservice)
      * [`obj spec.containers.livenessProbe.httpGet`](#obj-speccontainerslivenessprobehttpget)
        * [`fn withHost(host)`](#fn-speccontainerslivenessprobehttpgetwithhost)
        * [`fn withHttpHeaders(httpHeaders)`](#fn-speccontainerslivenessprobehttpgetwithhttpheaders)
        * [`fn withHttpHeadersMixin(httpHeaders)`](#fn-speccontainerslivenessprobehttpgetwithhttpheadersmixin)
        * [`fn withPath(path)`](#fn-speccontainerslivenessprobehttpgetwithpath)
        * [`fn withPort(port)`](#fn-speccontainerslivenessprobehttpgetwithport)
        * [`fn withScheme(scheme)`](#fn-speccontainerslivenessprobehttpgetwithscheme)
        * [`obj spec.containers.livenessProbe.httpGet.httpHeaders`](#obj-speccontainerslivenessprobehttpgethttpheaders)
          * [`fn withName(name)`](#fn-speccontainerslivenessprobehttpgethttpheaderswithname)
          * [`fn withValue(value)`](#fn-speccontainerslivenessprobehttpgethttpheaderswithvalue)
      * [`obj spec.containers.livenessProbe.tcpSocket`](#obj-speccontainerslivenessprobetcpsocket)
        * [`fn withHost(host)`](#fn-speccontainerslivenessprobetcpsocketwithhost)
        * [`fn withPort(port)`](#fn-speccontainerslivenessprobetcpsocketwithport)
    * [`obj spec.containers.ports`](#obj-speccontainersports)
      * [`fn withContainerPort(containerPort)`](#fn-speccontainersportswithcontainerport)
      * [`fn withName(name)`](#fn-speccontainersportswithname)
      * [`fn withProtocol(protocol)`](#fn-speccontainersportswithprotocol)
    * [`obj spec.containers.readinessProbe`](#obj-speccontainersreadinessprobe)
      * [`fn withFailureThreshold(failureThreshold)`](#fn-speccontainersreadinessprobewithfailurethreshold)
      * [`fn withInitialDelaySeconds(initialDelaySeconds)`](#fn-speccontainersreadinessprobewithinitialdelayseconds)
      * [`fn withPeriodSeconds(periodSeconds)`](#fn-speccontainersreadinessprobewithperiodseconds)
      * [`fn withSuccessThreshold(successThreshold)`](#fn-speccontainersreadinessprobewithsuccessthreshold)
      * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-speccontainersreadinessprobewithtimeoutseconds)
      * [`obj spec.containers.readinessProbe.exec`](#obj-speccontainersreadinessprobeexec)
        * [`fn withCommand(command)`](#fn-speccontainersreadinessprobeexecwithcommand)
        * [`fn withCommandMixin(command)`](#fn-speccontainersreadinessprobeexecwithcommandmixin)
      * [`obj spec.containers.readinessProbe.grpc`](#obj-speccontainersreadinessprobegrpc)
        * [`fn withPort(port)`](#fn-speccontainersreadinessprobegrpcwithport)
        * [`fn withService(service)`](#fn-speccontainersreadinessprobegrpcwithservice)
      * [`obj spec.containers.readinessProbe.httpGet`](#obj-speccontainersreadinessprobehttpget)
        * [`fn withHost(host)`](#fn-speccontainersreadinessprobehttpgetwithhost)
        * [`fn withHttpHeaders(httpHeaders)`](#fn-speccontainersreadinessprobehttpgetwithhttpheaders)
        * [`fn withHttpHeadersMixin(httpHeaders)`](#fn-speccontainersreadinessprobehttpgetwithhttpheadersmixin)
        * [`fn withPath(path)`](#fn-speccontainersreadinessprobehttpgetwithpath)
        * [`fn withPort(port)`](#fn-speccontainersreadinessprobehttpgetwithport)
        * [`fn withScheme(scheme)`](#fn-speccontainersreadinessprobehttpgetwithscheme)
        * [`obj spec.containers.readinessProbe.httpGet.httpHeaders`](#obj-speccontainersreadinessprobehttpgethttpheaders)
          * [`fn withName(name)`](#fn-speccontainersreadinessprobehttpgethttpheaderswithname)
          * [`fn withValue(value)`](#fn-speccontainersreadinessprobehttpgethttpheaderswithvalue)
      * [`obj spec.containers.readinessProbe.tcpSocket`](#obj-speccontainersreadinessprobetcpsocket)
        * [`fn withHost(host)`](#fn-speccontainersreadinessprobetcpsocketwithhost)
        * [`fn withPort(port)`](#fn-speccontainersreadinessprobetcpsocketwithport)
    * [`obj spec.containers.resources`](#obj-speccontainersresources)
      * [`fn withClaims(claims)`](#fn-speccontainersresourceswithclaims)
      * [`fn withClaimsMixin(claims)`](#fn-speccontainersresourceswithclaimsmixin)
      * [`fn withLimits(limits)`](#fn-speccontainersresourceswithlimits)
      * [`fn withLimitsMixin(limits)`](#fn-speccontainersresourceswithlimitsmixin)
      * [`fn withRequests(requests)`](#fn-speccontainersresourceswithrequests)
      * [`fn withRequestsMixin(requests)`](#fn-speccontainersresourceswithrequestsmixin)
      * [`obj spec.containers.resources.claims`](#obj-speccontainersresourcesclaims)
        * [`fn withName(name)`](#fn-speccontainersresourcesclaimswithname)
    * [`obj spec.containers.securityContext`](#obj-speccontainerssecuritycontext)
      * [`fn withAllowPrivilegeEscalation(allowPrivilegeEscalation)`](#fn-speccontainerssecuritycontextwithallowprivilegeescalation)
      * [`fn withReadOnlyRootFilesystem(readOnlyRootFilesystem)`](#fn-speccontainerssecuritycontextwithreadonlyrootfilesystem)
      * [`fn withRunAsGroup(runAsGroup)`](#fn-speccontainerssecuritycontextwithrunasgroup)
      * [`fn withRunAsNonRoot(runAsNonRoot)`](#fn-speccontainerssecuritycontextwithrunasnonroot)
      * [`fn withRunAsUser(runAsUser)`](#fn-speccontainerssecuritycontextwithrunasuser)
      * [`obj spec.containers.securityContext.capabilities`](#obj-speccontainerssecuritycontextcapabilities)
        * [`fn withAdd(add)`](#fn-speccontainerssecuritycontextcapabilitieswithadd)
        * [`fn withAddMixin(add)`](#fn-speccontainerssecuritycontextcapabilitieswithaddmixin)
        * [`fn withDrop(drop)`](#fn-speccontainerssecuritycontextcapabilitieswithdrop)
        * [`fn withDropMixin(drop)`](#fn-speccontainerssecuritycontextcapabilitieswithdropmixin)
      * [`obj spec.containers.securityContext.seccompProfile`](#obj-speccontainerssecuritycontextseccompprofile)
        * [`fn withLocalhostProfile(localhostProfile)`](#fn-speccontainerssecuritycontextseccompprofilewithlocalhostprofile)
        * [`fn withType(type)`](#fn-speccontainerssecuritycontextseccompprofilewithtype)
    * [`obj spec.containers.startupProbe`](#obj-speccontainersstartupprobe)
      * [`fn withFailureThreshold(failureThreshold)`](#fn-speccontainersstartupprobewithfailurethreshold)
      * [`fn withInitialDelaySeconds(initialDelaySeconds)`](#fn-speccontainersstartupprobewithinitialdelayseconds)
      * [`fn withPeriodSeconds(periodSeconds)`](#fn-speccontainersstartupprobewithperiodseconds)
      * [`fn withSuccessThreshold(successThreshold)`](#fn-speccontainersstartupprobewithsuccessthreshold)
      * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-speccontainersstartupprobewithtimeoutseconds)
      * [`obj spec.containers.startupProbe.exec`](#obj-speccontainersstartupprobeexec)
        * [`fn withCommand(command)`](#fn-speccontainersstartupprobeexecwithcommand)
        * [`fn withCommandMixin(command)`](#fn-speccontainersstartupprobeexecwithcommandmixin)
      * [`obj spec.containers.startupProbe.grpc`](#obj-speccontainersstartupprobegrpc)
        * [`fn withPort(port)`](#fn-speccontainersstartupprobegrpcwithport)
        * [`fn withService(service)`](#fn-speccontainersstartupprobegrpcwithservice)
      * [`obj spec.containers.startupProbe.httpGet`](#obj-speccontainersstartupprobehttpget)
        * [`fn withHost(host)`](#fn-speccontainersstartupprobehttpgetwithhost)
        * [`fn withHttpHeaders(httpHeaders)`](#fn-speccontainersstartupprobehttpgetwithhttpheaders)
        * [`fn withHttpHeadersMixin(httpHeaders)`](#fn-speccontainersstartupprobehttpgetwithhttpheadersmixin)
        * [`fn withPath(path)`](#fn-speccontainersstartupprobehttpgetwithpath)
        * [`fn withPort(port)`](#fn-speccontainersstartupprobehttpgetwithport)
        * [`fn withScheme(scheme)`](#fn-speccontainersstartupprobehttpgetwithscheme)
        * [`obj spec.containers.startupProbe.httpGet.httpHeaders`](#obj-speccontainersstartupprobehttpgethttpheaders)
          * [`fn withName(name)`](#fn-speccontainersstartupprobehttpgethttpheaderswithname)
          * [`fn withValue(value)`](#fn-speccontainersstartupprobehttpgethttpheaderswithvalue)
      * [`obj spec.containers.startupProbe.tcpSocket`](#obj-speccontainersstartupprobetcpsocket)
        * [`fn withHost(host)`](#fn-speccontainersstartupprobetcpsocketwithhost)
        * [`fn withPort(port)`](#fn-speccontainersstartupprobetcpsocketwithport)
    * [`obj spec.containers.volumeMounts`](#obj-speccontainersvolumemounts)
      * [`fn withMountPath(mountPath)`](#fn-speccontainersvolumemountswithmountpath)
      * [`fn withName(name)`](#fn-speccontainersvolumemountswithname)
      * [`fn withReadOnly(readOnly)`](#fn-speccontainersvolumemountswithreadonly)
      * [`fn withSubPath(subPath)`](#fn-speccontainersvolumemountswithsubpath)
  * [`obj spec.imagePullSecrets`](#obj-specimagepullsecrets)
    * [`fn withName(name)`](#fn-specimagepullsecretswithname)
  * [`obj spec.volumes`](#obj-specvolumes)
    * [`fn withEmptyDir(emptyDir)`](#fn-specvolumeswithemptydir)
    * [`fn withEmptyDirMixin(emptyDir)`](#fn-specvolumeswithemptydirmixin)
    * [`fn withName(name)`](#fn-specvolumeswithname)
    * [`fn withPersistentVolumeClaim(persistentVolumeClaim)`](#fn-specvolumeswithpersistentvolumeclaim)
    * [`fn withPersistentVolumeClaimMixin(persistentVolumeClaim)`](#fn-specvolumeswithpersistentvolumeclaimmixin)
    * [`obj spec.volumes.configMap`](#obj-specvolumesconfigmap)
      * [`fn withDefaultMode(defaultMode)`](#fn-specvolumesconfigmapwithdefaultmode)
      * [`fn withItems(items)`](#fn-specvolumesconfigmapwithitems)
      * [`fn withItemsMixin(items)`](#fn-specvolumesconfigmapwithitemsmixin)
      * [`fn withName(name)`](#fn-specvolumesconfigmapwithname)
      * [`fn withOptional(optional)`](#fn-specvolumesconfigmapwithoptional)
      * [`obj spec.volumes.configMap.items`](#obj-specvolumesconfigmapitems)
        * [`fn withKey(key)`](#fn-specvolumesconfigmapitemswithkey)
        * [`fn withMode(mode)`](#fn-specvolumesconfigmapitemswithmode)
        * [`fn withPath(path)`](#fn-specvolumesconfigmapitemswithpath)
    * [`obj spec.volumes.projected`](#obj-specvolumesprojected)
      * [`fn withDefaultMode(defaultMode)`](#fn-specvolumesprojectedwithdefaultmode)
      * [`fn withSources(sources)`](#fn-specvolumesprojectedwithsources)
      * [`fn withSourcesMixin(sources)`](#fn-specvolumesprojectedwithsourcesmixin)
      * [`obj spec.volumes.projected.sources`](#obj-specvolumesprojectedsources)
        * [`obj spec.volumes.projected.sources.configMap`](#obj-specvolumesprojectedsourcesconfigmap)
          * [`fn withItems(items)`](#fn-specvolumesprojectedsourcesconfigmapwithitems)
          * [`fn withItemsMixin(items)`](#fn-specvolumesprojectedsourcesconfigmapwithitemsmixin)
          * [`fn withName(name)`](#fn-specvolumesprojectedsourcesconfigmapwithname)
          * [`fn withOptional(optional)`](#fn-specvolumesprojectedsourcesconfigmapwithoptional)
          * [`obj spec.volumes.projected.sources.configMap.items`](#obj-specvolumesprojectedsourcesconfigmapitems)
            * [`fn withKey(key)`](#fn-specvolumesprojectedsourcesconfigmapitemswithkey)
            * [`fn withMode(mode)`](#fn-specvolumesprojectedsourcesconfigmapitemswithmode)
            * [`fn withPath(path)`](#fn-specvolumesprojectedsourcesconfigmapitemswithpath)
        * [`obj spec.volumes.projected.sources.downwardAPI`](#obj-specvolumesprojectedsourcesdownwardapi)
          * [`fn withItems(items)`](#fn-specvolumesprojectedsourcesdownwardapiwithitems)
          * [`fn withItemsMixin(items)`](#fn-specvolumesprojectedsourcesdownwardapiwithitemsmixin)
          * [`obj spec.volumes.projected.sources.downwardAPI.items`](#obj-specvolumesprojectedsourcesdownwardapiitems)
            * [`fn withMode(mode)`](#fn-specvolumesprojectedsourcesdownwardapiitemswithmode)
            * [`fn withPath(path)`](#fn-specvolumesprojectedsourcesdownwardapiitemswithpath)
            * [`obj spec.volumes.projected.sources.downwardAPI.items.fieldRef`](#obj-specvolumesprojectedsourcesdownwardapiitemsfieldref)
              * [`fn withApiVersion(apiVersion)`](#fn-specvolumesprojectedsourcesdownwardapiitemsfieldrefwithapiversion)
              * [`fn withFieldPath(fieldPath)`](#fn-specvolumesprojectedsourcesdownwardapiitemsfieldrefwithfieldpath)
            * [`obj spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef`](#obj-specvolumesprojectedsourcesdownwardapiitemsresourcefieldref)
              * [`fn withContainerName(containerName)`](#fn-specvolumesprojectedsourcesdownwardapiitemsresourcefieldrefwithcontainername)
              * [`fn withDivisor(divisor)`](#fn-specvolumesprojectedsourcesdownwardapiitemsresourcefieldrefwithdivisor)
              * [`fn withResource(resource)`](#fn-specvolumesprojectedsourcesdownwardapiitemsresourcefieldrefwithresource)
        * [`obj spec.volumes.projected.sources.secret`](#obj-specvolumesprojectedsourcessecret)
          * [`fn withItems(items)`](#fn-specvolumesprojectedsourcessecretwithitems)
          * [`fn withItemsMixin(items)`](#fn-specvolumesprojectedsourcessecretwithitemsmixin)
          * [`fn withName(name)`](#fn-specvolumesprojectedsourcessecretwithname)
          * [`fn withOptional(optional)`](#fn-specvolumesprojectedsourcessecretwithoptional)
          * [`obj spec.volumes.projected.sources.secret.items`](#obj-specvolumesprojectedsourcessecretitems)
            * [`fn withKey(key)`](#fn-specvolumesprojectedsourcessecretitemswithkey)
            * [`fn withMode(mode)`](#fn-specvolumesprojectedsourcessecretitemswithmode)
            * [`fn withPath(path)`](#fn-specvolumesprojectedsourcessecretitemswithpath)
        * [`obj spec.volumes.projected.sources.serviceAccountToken`](#obj-specvolumesprojectedsourcesserviceaccounttoken)
          * [`fn withAudience(audience)`](#fn-specvolumesprojectedsourcesserviceaccounttokenwithaudience)
          * [`fn withExpirationSeconds(expirationSeconds)`](#fn-specvolumesprojectedsourcesserviceaccounttokenwithexpirationseconds)
          * [`fn withPath(path)`](#fn-specvolumesprojectedsourcesserviceaccounttokenwithpath)
    * [`obj spec.volumes.secret`](#obj-specvolumessecret)
      * [`fn withDefaultMode(defaultMode)`](#fn-specvolumessecretwithdefaultmode)
      * [`fn withItems(items)`](#fn-specvolumessecretwithitems)
      * [`fn withItemsMixin(items)`](#fn-specvolumessecretwithitemsmixin)
      * [`fn withOptional(optional)`](#fn-specvolumessecretwithoptional)
      * [`fn withSecretName(secretName)`](#fn-specvolumessecretwithsecretname)
      * [`obj spec.volumes.secret.items`](#obj-specvolumessecretitems)
        * [`fn withKey(key)`](#fn-specvolumessecretitemswithkey)
        * [`fn withMode(mode)`](#fn-specvolumessecretitemswithmode)
        * [`fn withPath(path)`](#fn-specvolumessecretitemswithpath)

## Fields

### fn new

```ts
new(name)
```

new returns an instance of Revision

## obj metadata

"ObjectMeta is metadata that all persisted resources must have, which includes all objects users must create."

### fn metadata.withAnnotations

```ts
withAnnotations(annotations)
```

"Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations"

### fn metadata.withAnnotationsMixin

```ts
withAnnotationsMixin(annotations)
```

"Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations"

**Note:** This function appends passed data to existing values

### fn metadata.withClusterName

```ts
withClusterName(clusterName)
```

"The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request."

### fn metadata.withCreationTimestamp

```ts
withCreationTimestamp(creationTimestamp)
```

"Time is a wrapper around time.Time which supports correct marshaling to YAML and JSON.  Wrappers are provided for many of the factory methods that the time package offers."

### fn metadata.withDeletionGracePeriodSeconds

```ts
withDeletionGracePeriodSeconds(deletionGracePeriodSeconds)
```

"Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only."

### fn metadata.withDeletionTimestamp

```ts
withDeletionTimestamp(deletionTimestamp)
```

"Time is a wrapper around time.Time which supports correct marshaling to YAML and JSON.  Wrappers are provided for many of the factory methods that the time package offers."

### fn metadata.withFinalizers

```ts
withFinalizers(finalizers)
```

"Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed. Finalizers may be processed and removed in any order.  Order is NOT enforced because it introduces significant risk of stuck finalizers. finalizers is a shared field, any actor with permission can reorder it. If the finalizer list is processed in order, then this can lead to a situation in which the component responsible for the first finalizer in the list is waiting for a signal (field value, external system, or other) produced by a component responsible for a finalizer later in the list, resulting in a deadlock. Without enforced ordering finalizers are free to order amongst themselves and are not vulnerable to ordering changes in the list."

### fn metadata.withFinalizersMixin

```ts
withFinalizersMixin(finalizers)
```

"Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed. Finalizers may be processed and removed in any order.  Order is NOT enforced because it introduces significant risk of stuck finalizers. finalizers is a shared field, any actor with permission can reorder it. If the finalizer list is processed in order, then this can lead to a situation in which the component responsible for the first finalizer in the list is waiting for a signal (field value, external system, or other) produced by a component responsible for a finalizer later in the list, resulting in a deadlock. Without enforced ordering finalizers are free to order amongst themselves and are not vulnerable to ordering changes in the list."

**Note:** This function appends passed data to existing values

### fn metadata.withGenerateName

```ts
withGenerateName(generateName)
```

"GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.\n\nIf this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).\n\nApplied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#idempotency"

### fn metadata.withGeneration

```ts
withGeneration(generation)
```

"A sequence number representing a specific generation of the desired state. Populated by the system. Read-only."

### fn metadata.withLabels

```ts
withLabels(labels)
```

"Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels"

### fn metadata.withLabelsMixin

```ts
withLabelsMixin(labels)
```

"Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels"

**Note:** This function appends passed data to existing values

### fn metadata.withName

```ts
withName(name)
```

"Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names"

### fn metadata.withNamespace

```ts
withNamespace(namespace)
```

"Namespace defines the space within which each name must be unique. An empty namespace is equivalent to the \"default\" namespace, but \"default\" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.\n\nMust be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces"

### fn metadata.withOwnerReferences

```ts
withOwnerReferences(ownerReferences)
```

"List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller."

### fn metadata.withOwnerReferencesMixin

```ts
withOwnerReferencesMixin(ownerReferences)
```

"List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller."

**Note:** This function appends passed data to existing values

### fn metadata.withResourceVersion

```ts
withResourceVersion(resourceVersion)
```

"An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.\n\nPopulated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#concurrency-control-and-consistency"

### fn metadata.withSelfLink

```ts
withSelfLink(selfLink)
```

"SelfLink is a URL representing this object. Populated by the system. Read-only.\n\nDEPRECATED Kubernetes will stop propagating this field in 1.20 release and the field is planned to be removed in 1.21 release."

### fn metadata.withUid

```ts
withUid(uid)
```

"UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.\n\nPopulated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids"

## obj spec

"RevisionSpec holds the desired state of the Revision (from the client)."

### fn spec.withAffinity

```ts
withAffinity(affinity)
```

"This is accessible behind a feature flag - kubernetes.podspec-affinity"

### fn spec.withAffinityMixin

```ts
withAffinityMixin(affinity)
```

"This is accessible behind a feature flag - kubernetes.podspec-affinity"

**Note:** This function appends passed data to existing values

### fn spec.withAutomountServiceAccountToken

```ts
withAutomountServiceAccountToken(automountServiceAccountToken)
```

"AutomountServiceAccountToken indicates whether a service account token should be automatically mounted."

### fn spec.withContainerConcurrency

```ts
withContainerConcurrency(containerConcurrency)
```

"ContainerConcurrency specifies the maximum allowed in-flight (concurrent)\nrequests per container of the Revision.  Defaults to `0` which means\nconcurrency to the application is not limited, and the system decides the\ntarget concurrency for the autoscaler."

### fn spec.withContainers

```ts
withContainers(containers)
```

"List of containers belonging to the pod.\nContainers cannot currently be added or removed.\nThere must be at least one container in a Pod.\nCannot be updated."

### fn spec.withContainersMixin

```ts
withContainersMixin(containers)
```

"List of containers belonging to the pod.\nContainers cannot currently be added or removed.\nThere must be at least one container in a Pod.\nCannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.withDnsConfig

```ts
withDnsConfig(dnsConfig)
```

"This is accessible behind a feature flag - kubernetes.podspec-dnsconfig"

### fn spec.withDnsConfigMixin

```ts
withDnsConfigMixin(dnsConfig)
```

"This is accessible behind a feature flag - kubernetes.podspec-dnsconfig"

**Note:** This function appends passed data to existing values

### fn spec.withDnsPolicy

```ts
withDnsPolicy(dnsPolicy)
```

"This is accessible behind a feature flag - kubernetes.podspec-dnspolicy"

### fn spec.withEnableServiceLinks

```ts
withEnableServiceLinks(enableServiceLinks)
```

"EnableServiceLinks indicates whether information about services should be injected into pod's environment variables, matching the syntax of Docker links. Optional: Knative defaults this to false."

### fn spec.withHostAliases

```ts
withHostAliases(hostAliases)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostaliases"

### fn spec.withHostAliasesMixin

```ts
withHostAliasesMixin(hostAliases)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostaliases"

**Note:** This function appends passed data to existing values

### fn spec.withHostIPC

```ts
withHostIPC(hostIPC)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostipc"

### fn spec.withHostNetwork

```ts
withHostNetwork(hostNetwork)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostnetwork"

### fn spec.withHostPID

```ts
withHostPID(hostPID)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostpid"

### fn spec.withIdleTimeoutSeconds

```ts
withIdleTimeoutSeconds(idleTimeoutSeconds)
```

"IdleTimeoutSeconds is the maximum duration in seconds a request will be allowed\nto stay open while not receiving any bytes from the user's application. If\nunspecified, a system default will be provided."

### fn spec.withImagePullSecrets

```ts
withImagePullSecrets(imagePullSecrets)
```

"ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec.\nIf specified, these secrets will be passed to individual puller implementations for them to use.\nMore info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod"

### fn spec.withImagePullSecretsMixin

```ts
withImagePullSecretsMixin(imagePullSecrets)
```

"ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec.\nIf specified, these secrets will be passed to individual puller implementations for them to use.\nMore info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod"

**Note:** This function appends passed data to existing values

### fn spec.withInitContainers

```ts
withInitContainers(initContainers)
```

"List of initialization containers belonging to the pod.\nInit containers are executed in order prior to containers being started. If any\ninit container fails, the pod is considered to have failed and is handled according\nto its restartPolicy. The name for an init container or normal container must be\nunique among all containers.\nInit containers may not have Lifecycle actions, Readiness probes, Liveness probes, or Startup probes.\nThe resourceRequirements of an init container are taken into account during scheduling\nby finding the highest request/limit for each resource type, and then using the max of\nof that value or the sum of the normal containers. Limits are applied to init containers\nin a similar fashion.\nInit containers cannot currently be added or removed.\nCannot be updated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/"

### fn spec.withInitContainersMixin

```ts
withInitContainersMixin(initContainers)
```

"List of initialization containers belonging to the pod.\nInit containers are executed in order prior to containers being started. If any\ninit container fails, the pod is considered to have failed and is handled according\nto its restartPolicy. The name for an init container or normal container must be\nunique among all containers.\nInit containers may not have Lifecycle actions, Readiness probes, Liveness probes, or Startup probes.\nThe resourceRequirements of an init container are taken into account during scheduling\nby finding the highest request/limit for each resource type, and then using the max of\nof that value or the sum of the normal containers. Limits are applied to init containers\nin a similar fashion.\nInit containers cannot currently be added or removed.\nCannot be updated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/"

**Note:** This function appends passed data to existing values

### fn spec.withNodeSelector

```ts
withNodeSelector(nodeSelector)
```

"This is accessible behind a feature flag - kubernetes.podspec-nodeselector"

### fn spec.withNodeSelectorMixin

```ts
withNodeSelectorMixin(nodeSelector)
```

"This is accessible behind a feature flag - kubernetes.podspec-nodeselector"

**Note:** This function appends passed data to existing values

### fn spec.withPriorityClassName

```ts
withPriorityClassName(priorityClassName)
```

"This is accessible behind a feature flag - kubernetes.podspec-priorityclassname"

### fn spec.withResponseStartTimeoutSeconds

```ts
withResponseStartTimeoutSeconds(responseStartTimeoutSeconds)
```

"ResponseStartTimeoutSeconds is the maximum duration in seconds that the request\nrouting layer will wait for a request delivered to a container to begin\nsending any network traffic."

### fn spec.withRuntimeClassName

```ts
withRuntimeClassName(runtimeClassName)
```

"This is accessible behind a feature flag - kubernetes.podspec-runtimeclassname"

### fn spec.withSchedulerName

```ts
withSchedulerName(schedulerName)
```

"This is accessible behind a feature flag - kubernetes.podspec-schedulername"

### fn spec.withSecurityContext

```ts
withSecurityContext(securityContext)
```

"This is accessible behind a feature flag - kubernetes.podspec-securitycontext"

### fn spec.withSecurityContextMixin

```ts
withSecurityContextMixin(securityContext)
```

"This is accessible behind a feature flag - kubernetes.podspec-securitycontext"

**Note:** This function appends passed data to existing values

### fn spec.withServiceAccountName

```ts
withServiceAccountName(serviceAccountName)
```

"ServiceAccountName is the name of the ServiceAccount to use to run this pod.\nMore info: https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/"

### fn spec.withShareProcessNamespace

```ts
withShareProcessNamespace(shareProcessNamespace)
```

"This is accessible behind a feature flag - kubernetes.podspec-shareproccessnamespace"

### fn spec.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"TimeoutSeconds is the maximum duration in seconds that the request instance\nis allowed to respond to a request. If unspecified, a system default will\nbe provided."

### fn spec.withTolerations

```ts
withTolerations(tolerations)
```

"This is accessible behind a feature flag - kubernetes.podspec-tolerations"

### fn spec.withTolerationsMixin

```ts
withTolerationsMixin(tolerations)
```

"This is accessible behind a feature flag - kubernetes.podspec-tolerations"

**Note:** This function appends passed data to existing values

### fn spec.withTopologySpreadConstraints

```ts
withTopologySpreadConstraints(topologySpreadConstraints)
```

"This is accessible behind a feature flag - kubernetes.podspec-topologyspreadconstraints"

### fn spec.withTopologySpreadConstraintsMixin

```ts
withTopologySpreadConstraintsMixin(topologySpreadConstraints)
```

"This is accessible behind a feature flag - kubernetes.podspec-topologyspreadconstraints"

**Note:** This function appends passed data to existing values

### fn spec.withVolumes

```ts
withVolumes(volumes)
```

"List of volumes that can be mounted by containers belonging to the pod.\nMore info: https://kubernetes.io/docs/concepts/storage/volumes"

### fn spec.withVolumesMixin

```ts
withVolumesMixin(volumes)
```

"List of volumes that can be mounted by containers belonging to the pod.\nMore info: https://kubernetes.io/docs/concepts/storage/volumes"

**Note:** This function appends passed data to existing values

## obj spec.containers

"List of containers belonging to the pod.\nContainers cannot currently be added or removed.\nThere must be at least one container in a Pod.\nCannot be updated."

### fn spec.containers.withArgs

```ts
withArgs(args)
```

"Arguments to the entrypoint.\nThe container image's CMD is used if this is not provided.\nVariable references $(VAR_NAME) are expanded using the container's environment. If a variable\ncannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced\nto a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will\nproduce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless\nof whether the variable exists or not. Cannot be updated.\nMore info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

### fn spec.containers.withArgsMixin

```ts
withArgsMixin(args)
```

"Arguments to the entrypoint.\nThe container image's CMD is used if this is not provided.\nVariable references $(VAR_NAME) are expanded using the container's environment. If a variable\ncannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced\nto a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will\nproduce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless\nof whether the variable exists or not. Cannot be updated.\nMore info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

**Note:** This function appends passed data to existing values

### fn spec.containers.withCommand

```ts
withCommand(command)
```

"Entrypoint array. Not executed within a shell.\nThe container image's ENTRYPOINT is used if this is not provided.\nVariable references $(VAR_NAME) are expanded using the container's environment. If a variable\ncannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced\nto a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will\nproduce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless\nof whether the variable exists or not. Cannot be updated.\nMore info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

### fn spec.containers.withCommandMixin

```ts
withCommandMixin(command)
```

"Entrypoint array. Not executed within a shell.\nThe container image's ENTRYPOINT is used if this is not provided.\nVariable references $(VAR_NAME) are expanded using the container's environment. If a variable\ncannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced\nto a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will\nproduce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless\nof whether the variable exists or not. Cannot be updated.\nMore info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

**Note:** This function appends passed data to existing values

### fn spec.containers.withEnv

```ts
withEnv(env)
```

"List of environment variables to set in the container.\nCannot be updated."

### fn spec.containers.withEnvFrom

```ts
withEnvFrom(envFrom)
```

"List of sources to populate environment variables in the container.\nThe keys defined within a source must be a C_IDENTIFIER. All invalid keys\nwill be reported as an event when the container is starting. When a key exists in multiple\nsources, the value associated with the last source will take precedence.\nValues defined by an Env with a duplicate key will take precedence.\nCannot be updated."

### fn spec.containers.withEnvFromMixin

```ts
withEnvFromMixin(envFrom)
```

"List of sources to populate environment variables in the container.\nThe keys defined within a source must be a C_IDENTIFIER. All invalid keys\nwill be reported as an event when the container is starting. When a key exists in multiple\nsources, the value associated with the last source will take precedence.\nValues defined by an Env with a duplicate key will take precedence.\nCannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.containers.withEnvMixin

```ts
withEnvMixin(env)
```

"List of environment variables to set in the container.\nCannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.containers.withImage

```ts
withImage(image)
```

"Container image name.\nMore info: https://kubernetes.io/docs/concepts/containers/images\nThis field is optional to allow higher level config management to default or override\ncontainer images in workload controllers like Deployments and StatefulSets."

### fn spec.containers.withImagePullPolicy

```ts
withImagePullPolicy(imagePullPolicy)
```

"Image pull policy.\nOne of Always, Never, IfNotPresent.\nDefaults to Always if :latest tag is specified, or IfNotPresent otherwise.\nCannot be updated.\nMore info: https://kubernetes.io/docs/concepts/containers/images#updating-images"

### fn spec.containers.withName

```ts
withName(name)
```

"Name of the container specified as a DNS_LABEL.\nEach container in a pod must have a unique name (DNS_LABEL).\nCannot be updated."

### fn spec.containers.withPorts

```ts
withPorts(ports)
```

"List of ports to expose from the container. Not specifying a port here\nDOES NOT prevent that port from being exposed. Any port which is\nlistening on the default \"0.0.0.0\" address inside a container will be\naccessible from the network.\nModifying this array with strategic merge patch may corrupt the data.\nFor more information See https://github.com/kubernetes/kubernetes/issues/108255.\nCannot be updated."

### fn spec.containers.withPortsMixin

```ts
withPortsMixin(ports)
```

"List of ports to expose from the container. Not specifying a port here\nDOES NOT prevent that port from being exposed. Any port which is\nlistening on the default \"0.0.0.0\" address inside a container will be\naccessible from the network.\nModifying this array with strategic merge patch may corrupt the data.\nFor more information See https://github.com/kubernetes/kubernetes/issues/108255.\nCannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.containers.withTerminationMessagePath

```ts
withTerminationMessagePath(terminationMessagePath)
```

"Optional: Path at which the file to which the container's termination message\nwill be written is mounted into the container's filesystem.\nMessage written is intended to be brief final status, such as an assertion failure message.\nWill be truncated by the node if greater than 4096 bytes. The total message length across\nall containers will be limited to 12kb.\nDefaults to /dev/termination-log.\nCannot be updated."

### fn spec.containers.withTerminationMessagePolicy

```ts
withTerminationMessagePolicy(terminationMessagePolicy)
```

"Indicate how the termination message should be populated. File will use the contents of\nterminationMessagePath to populate the container status message on both success and failure.\nFallbackToLogsOnError will use the last chunk of container log output if the termination\nmessage file is empty and the container exited with an error.\nThe log output is limited to 2048 bytes or 80 lines, whichever is smaller.\nDefaults to File.\nCannot be updated."

### fn spec.containers.withVolumeMounts

```ts
withVolumeMounts(volumeMounts)
```

"Pod volumes to mount into the container's filesystem.\nCannot be updated."

### fn spec.containers.withVolumeMountsMixin

```ts
withVolumeMountsMixin(volumeMounts)
```

"Pod volumes to mount into the container's filesystem.\nCannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.containers.withWorkingDir

```ts
withWorkingDir(workingDir)
```

"Container's working directory.\nIf not specified, the container runtime's default will be used, which\nmight be configured in the container image.\nCannot be updated."

## obj spec.containers.env

"List of environment variables to set in the container.\nCannot be updated."

### fn spec.containers.env.withName

```ts
withName(name)
```

"Name of the environment variable. Must be a C_IDENTIFIER."

### fn spec.containers.env.withValue

```ts
withValue(value)
```

"Variable references $(VAR_NAME) are expanded\nusing the previously defined environment variables in the container and\nany service environment variables. If a variable cannot be resolved,\nthe reference in the input string will be unchanged. Double $$ are reduced\nto a single $, which allows for escaping the $(VAR_NAME) syntax: i.e.\n\"$$(VAR_NAME)\" will produce the string literal \"$(VAR_NAME)\".\nEscaped references will never be expanded, regardless of whether the variable\nexists or not.\nDefaults to \"\"."

## obj spec.containers.env.valueFrom

"Source for the environment variable's value. Cannot be used if value is not empty."

### fn spec.containers.env.valueFrom.withFieldRef

```ts
withFieldRef(fieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

### fn spec.containers.env.valueFrom.withFieldRefMixin

```ts
withFieldRefMixin(fieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

**Note:** This function appends passed data to existing values

### fn spec.containers.env.valueFrom.withResourceFieldRef

```ts
withResourceFieldRef(resourceFieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

### fn spec.containers.env.valueFrom.withResourceFieldRefMixin

```ts
withResourceFieldRefMixin(resourceFieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

**Note:** This function appends passed data to existing values

## obj spec.containers.env.valueFrom.configMapKeyRef

"Selects a key of a ConfigMap."

### fn spec.containers.env.valueFrom.configMapKeyRef.withKey

```ts
withKey(key)
```

"The key to select."

### fn spec.containers.env.valueFrom.configMapKeyRef.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.containers.env.valueFrom.configMapKeyRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the ConfigMap or its key must be defined"

## obj spec.containers.env.valueFrom.secretKeyRef

"Selects a key of a secret in the pod's namespace"

### fn spec.containers.env.valueFrom.secretKeyRef.withKey

```ts
withKey(key)
```

"The key of the secret to select from.  Must be a valid secret key."

### fn spec.containers.env.valueFrom.secretKeyRef.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.containers.env.valueFrom.secretKeyRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the Secret or its key must be defined"

## obj spec.containers.envFrom

"List of sources to populate environment variables in the container.\nThe keys defined within a source must be a C_IDENTIFIER. All invalid keys\nwill be reported as an event when the container is starting. When a key exists in multiple\nsources, the value associated with the last source will take precedence.\nValues defined by an Env with a duplicate key will take precedence.\nCannot be updated."

### fn spec.containers.envFrom.withPrefix

```ts
withPrefix(prefix)
```

"An optional identifier to prepend to each key in the ConfigMap. Must be a C_IDENTIFIER."

## obj spec.containers.envFrom.configMapRef

"The ConfigMap to select from"

### fn spec.containers.envFrom.configMapRef.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.containers.envFrom.configMapRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the ConfigMap must be defined"

## obj spec.containers.envFrom.secretRef

"The Secret to select from"

### fn spec.containers.envFrom.secretRef.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.containers.envFrom.secretRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the Secret must be defined"

## obj spec.containers.livenessProbe

"Periodic probe of container liveness.\nContainer will be restarted if the probe fails.\nCannot be updated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.containers.livenessProbe.withFailureThreshold

```ts
withFailureThreshold(failureThreshold)
```

"Minimum consecutive failures for the probe to be considered failed after having succeeded.\nDefaults to 3. Minimum value is 1."

### fn spec.containers.livenessProbe.withInitialDelaySeconds

```ts
withInitialDelaySeconds(initialDelaySeconds)
```

"Number of seconds after the container has started before liveness probes are initiated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.containers.livenessProbe.withPeriodSeconds

```ts
withPeriodSeconds(periodSeconds)
```

"How often (in seconds) to perform the probe."

### fn spec.containers.livenessProbe.withSuccessThreshold

```ts
withSuccessThreshold(successThreshold)
```

"Minimum consecutive successes for the probe to be considered successful after having failed.\nDefaults to 1. Must be 1 for liveness and startup. Minimum value is 1."

### fn spec.containers.livenessProbe.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"Number of seconds after which the probe times out.\nDefaults to 1 second. Minimum value is 1.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

## obj spec.containers.livenessProbe.exec

"Exec specifies the action to take."

### fn spec.containers.livenessProbe.exec.withCommand

```ts
withCommand(command)
```

"Command is the command line to execute inside the container, the working directory for the\ncommand  is root ('/') in the container's filesystem. The command is simply exec'd, it is\nnot run inside a shell, so traditional shell instructions ('|', etc) won't work. To use\na shell, you need to explicitly call out to that shell.\nExit status of 0 is treated as live/healthy and non-zero is unhealthy."

### fn spec.containers.livenessProbe.exec.withCommandMixin

```ts
withCommandMixin(command)
```

"Command is the command line to execute inside the container, the working directory for the\ncommand  is root ('/') in the container's filesystem. The command is simply exec'd, it is\nnot run inside a shell, so traditional shell instructions ('|', etc) won't work. To use\na shell, you need to explicitly call out to that shell.\nExit status of 0 is treated as live/healthy and non-zero is unhealthy."

**Note:** This function appends passed data to existing values

## obj spec.containers.livenessProbe.grpc

"GRPC specifies an action involving a GRPC port."

### fn spec.containers.livenessProbe.grpc.withPort

```ts
withPort(port)
```

"Port number of the gRPC service. Number must be in the range 1 to 65535."

### fn spec.containers.livenessProbe.grpc.withService

```ts
withService(service)
```

"Service is the name of the service to place in the gRPC HealthCheckRequest\n(see https://github.com/grpc/grpc/blob/master/doc/health-checking.md).\n\n\nIf this is not specified, the default behavior is defined by gRPC."

## obj spec.containers.livenessProbe.httpGet

"HTTPGet specifies the http request to perform."

### fn spec.containers.livenessProbe.httpGet.withHost

```ts
withHost(host)
```

"Host name to connect to, defaults to the pod IP. You probably want to set\n\"Host\" in httpHeaders instead."

### fn spec.containers.livenessProbe.httpGet.withHttpHeaders

```ts
withHttpHeaders(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.containers.livenessProbe.httpGet.withHttpHeadersMixin

```ts
withHttpHeadersMixin(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

**Note:** This function appends passed data to existing values

### fn spec.containers.livenessProbe.httpGet.withPath

```ts
withPath(path)
```

"Path to access on the HTTP server."

### fn spec.containers.livenessProbe.httpGet.withPort

```ts
withPort(port)
```

"Name or number of the port to access on the container.\nNumber must be in the range 1 to 65535.\nName must be an IANA_SVC_NAME."

### fn spec.containers.livenessProbe.httpGet.withScheme

```ts
withScheme(scheme)
```

"Scheme to use for connecting to the host.\nDefaults to HTTP."

## obj spec.containers.livenessProbe.httpGet.httpHeaders

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.containers.livenessProbe.httpGet.httpHeaders.withName

```ts
withName(name)
```

"The header field name.\nThis will be canonicalized upon output, so case-variant names will be understood as the same header."

### fn spec.containers.livenessProbe.httpGet.httpHeaders.withValue

```ts
withValue(value)
```

"The header field value"

## obj spec.containers.livenessProbe.tcpSocket

"TCPSocket specifies an action involving a TCP port."

### fn spec.containers.livenessProbe.tcpSocket.withHost

```ts
withHost(host)
```

"Optional: Host name to connect to, defaults to the pod IP."

### fn spec.containers.livenessProbe.tcpSocket.withPort

```ts
withPort(port)
```

"Number or name of the port to access on the container.\nNumber must be in the range 1 to 65535.\nName must be an IANA_SVC_NAME."

## obj spec.containers.ports

"List of ports to expose from the container. Not specifying a port here\nDOES NOT prevent that port from being exposed. Any port which is\nlistening on the default \"0.0.0.0\" address inside a container will be\naccessible from the network.\nModifying this array with strategic merge patch may corrupt the data.\nFor more information See https://github.com/kubernetes/kubernetes/issues/108255.\nCannot be updated."

### fn spec.containers.ports.withContainerPort

```ts
withContainerPort(containerPort)
```

"Number of port to expose on the pod's IP address.\nThis must be a valid port number, 0 < x < 65536."

### fn spec.containers.ports.withName

```ts
withName(name)
```

"If specified, this must be an IANA_SVC_NAME and unique within the pod. Each\nnamed port in a pod must have a unique name. Name for the port that can be\nreferred to by services."

### fn spec.containers.ports.withProtocol

```ts
withProtocol(protocol)
```

"Protocol for port. Must be UDP, TCP, or SCTP.\nDefaults to \"TCP\"."

## obj spec.containers.readinessProbe

"Periodic probe of container service readiness.\nContainer will be removed from service endpoints if the probe fails.\nCannot be updated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.containers.readinessProbe.withFailureThreshold

```ts
withFailureThreshold(failureThreshold)
```

"Minimum consecutive failures for the probe to be considered failed after having succeeded.\nDefaults to 3. Minimum value is 1."

### fn spec.containers.readinessProbe.withInitialDelaySeconds

```ts
withInitialDelaySeconds(initialDelaySeconds)
```

"Number of seconds after the container has started before liveness probes are initiated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.containers.readinessProbe.withPeriodSeconds

```ts
withPeriodSeconds(periodSeconds)
```

"How often (in seconds) to perform the probe."

### fn spec.containers.readinessProbe.withSuccessThreshold

```ts
withSuccessThreshold(successThreshold)
```

"Minimum consecutive successes for the probe to be considered successful after having failed.\nDefaults to 1. Must be 1 for liveness and startup. Minimum value is 1."

### fn spec.containers.readinessProbe.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"Number of seconds after which the probe times out.\nDefaults to 1 second. Minimum value is 1.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

## obj spec.containers.readinessProbe.exec

"Exec specifies the action to take."

### fn spec.containers.readinessProbe.exec.withCommand

```ts
withCommand(command)
```

"Command is the command line to execute inside the container, the working directory for the\ncommand  is root ('/') in the container's filesystem. The command is simply exec'd, it is\nnot run inside a shell, so traditional shell instructions ('|', etc) won't work. To use\na shell, you need to explicitly call out to that shell.\nExit status of 0 is treated as live/healthy and non-zero is unhealthy."

### fn spec.containers.readinessProbe.exec.withCommandMixin

```ts
withCommandMixin(command)
```

"Command is the command line to execute inside the container, the working directory for the\ncommand  is root ('/') in the container's filesystem. The command is simply exec'd, it is\nnot run inside a shell, so traditional shell instructions ('|', etc) won't work. To use\na shell, you need to explicitly call out to that shell.\nExit status of 0 is treated as live/healthy and non-zero is unhealthy."

**Note:** This function appends passed data to existing values

## obj spec.containers.readinessProbe.grpc

"GRPC specifies an action involving a GRPC port."

### fn spec.containers.readinessProbe.grpc.withPort

```ts
withPort(port)
```

"Port number of the gRPC service. Number must be in the range 1 to 65535."

### fn spec.containers.readinessProbe.grpc.withService

```ts
withService(service)
```

"Service is the name of the service to place in the gRPC HealthCheckRequest\n(see https://github.com/grpc/grpc/blob/master/doc/health-checking.md).\n\n\nIf this is not specified, the default behavior is defined by gRPC."

## obj spec.containers.readinessProbe.httpGet

"HTTPGet specifies the http request to perform."

### fn spec.containers.readinessProbe.httpGet.withHost

```ts
withHost(host)
```

"Host name to connect to, defaults to the pod IP. You probably want to set\n\"Host\" in httpHeaders instead."

### fn spec.containers.readinessProbe.httpGet.withHttpHeaders

```ts
withHttpHeaders(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.containers.readinessProbe.httpGet.withHttpHeadersMixin

```ts
withHttpHeadersMixin(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

**Note:** This function appends passed data to existing values

### fn spec.containers.readinessProbe.httpGet.withPath

```ts
withPath(path)
```

"Path to access on the HTTP server."

### fn spec.containers.readinessProbe.httpGet.withPort

```ts
withPort(port)
```

"Name or number of the port to access on the container.\nNumber must be in the range 1 to 65535.\nName must be an IANA_SVC_NAME."

### fn spec.containers.readinessProbe.httpGet.withScheme

```ts
withScheme(scheme)
```

"Scheme to use for connecting to the host.\nDefaults to HTTP."

## obj spec.containers.readinessProbe.httpGet.httpHeaders

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.containers.readinessProbe.httpGet.httpHeaders.withName

```ts
withName(name)
```

"The header field name.\nThis will be canonicalized upon output, so case-variant names will be understood as the same header."

### fn spec.containers.readinessProbe.httpGet.httpHeaders.withValue

```ts
withValue(value)
```

"The header field value"

## obj spec.containers.readinessProbe.tcpSocket

"TCPSocket specifies an action involving a TCP port."

### fn spec.containers.readinessProbe.tcpSocket.withHost

```ts
withHost(host)
```

"Optional: Host name to connect to, defaults to the pod IP."

### fn spec.containers.readinessProbe.tcpSocket.withPort

```ts
withPort(port)
```

"Number or name of the port to access on the container.\nNumber must be in the range 1 to 65535.\nName must be an IANA_SVC_NAME."

## obj spec.containers.resources

"Compute Resources required by this container.\nCannot be updated.\nMore info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

### fn spec.containers.resources.withClaims

```ts
withClaims(claims)
```

"Claims lists the names of resources, defined in spec.resourceClaims,\nthat are used by this container.\n\n\nThis is an alpha field and requires enabling the\nDynamicResourceAllocation feature gate.\n\n\nThis field is immutable. It can only be set for containers."

### fn spec.containers.resources.withClaimsMixin

```ts
withClaimsMixin(claims)
```

"Claims lists the names of resources, defined in spec.resourceClaims,\nthat are used by this container.\n\n\nThis is an alpha field and requires enabling the\nDynamicResourceAllocation feature gate.\n\n\nThis field is immutable. It can only be set for containers."

**Note:** This function appends passed data to existing values

### fn spec.containers.resources.withLimits

```ts
withLimits(limits)
```

"Limits describes the maximum amount of compute resources allowed.\nMore info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

### fn spec.containers.resources.withLimitsMixin

```ts
withLimitsMixin(limits)
```

"Limits describes the maximum amount of compute resources allowed.\nMore info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

**Note:** This function appends passed data to existing values

### fn spec.containers.resources.withRequests

```ts
withRequests(requests)
```

"Requests describes the minimum amount of compute resources required.\nIf Requests is omitted for a container, it defaults to Limits if that is explicitly specified,\notherwise to an implementation-defined value. Requests cannot exceed Limits.\nMore info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

### fn spec.containers.resources.withRequestsMixin

```ts
withRequestsMixin(requests)
```

"Requests describes the minimum amount of compute resources required.\nIf Requests is omitted for a container, it defaults to Limits if that is explicitly specified,\notherwise to an implementation-defined value. Requests cannot exceed Limits.\nMore info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

**Note:** This function appends passed data to existing values

## obj spec.containers.resources.claims

"Claims lists the names of resources, defined in spec.resourceClaims,\nthat are used by this container.\n\n\nThis is an alpha field and requires enabling the\nDynamicResourceAllocation feature gate.\n\n\nThis field is immutable. It can only be set for containers."

### fn spec.containers.resources.claims.withName

```ts
withName(name)
```

"Name must match the name of one entry in pod.spec.resourceClaims of\nthe Pod where this field is used. It makes that resource available\ninside a container."

## obj spec.containers.securityContext

"SecurityContext defines the security options the container should be run with.\nIf set, the fields of SecurityContext override the equivalent fields of PodSecurityContext.\nMore info: https://kubernetes.io/docs/tasks/configure-pod-container/security-context/"

### fn spec.containers.securityContext.withAllowPrivilegeEscalation

```ts
withAllowPrivilegeEscalation(allowPrivilegeEscalation)
```

"AllowPrivilegeEscalation controls whether a process can gain more\nprivileges than its parent process. This bool directly controls if\nthe no_new_privs flag will be set on the container process.\nAllowPrivilegeEscalation is true always when the container is:\n1) run as Privileged\n2) has CAP_SYS_ADMIN\nNote that this field cannot be set when spec.os.name is windows."

### fn spec.containers.securityContext.withReadOnlyRootFilesystem

```ts
withReadOnlyRootFilesystem(readOnlyRootFilesystem)
```

"Whether this container has a read-only root filesystem.\nDefault is false.\nNote that this field cannot be set when spec.os.name is windows."

### fn spec.containers.securityContext.withRunAsGroup

```ts
withRunAsGroup(runAsGroup)
```

"The GID to run the entrypoint of the container process.\nUses runtime default if unset.\nMay also be set in PodSecurityContext.  If set in both SecurityContext and\nPodSecurityContext, the value specified in SecurityContext takes precedence.\nNote that this field cannot be set when spec.os.name is windows."

### fn spec.containers.securityContext.withRunAsNonRoot

```ts
withRunAsNonRoot(runAsNonRoot)
```

"Indicates that the container must run as a non-root user.\nIf true, the Kubelet will validate the image at runtime to ensure that it\ndoes not run as UID 0 (root) and fail to start the container if it does.\nIf unset or false, no such validation will be performed.\nMay also be set in PodSecurityContext.  If set in both SecurityContext and\nPodSecurityContext, the value specified in SecurityContext takes precedence."

### fn spec.containers.securityContext.withRunAsUser

```ts
withRunAsUser(runAsUser)
```

"The UID to run the entrypoint of the container process.\nDefaults to user specified in image metadata if unspecified.\nMay also be set in PodSecurityContext.  If set in both SecurityContext and\nPodSecurityContext, the value specified in SecurityContext takes precedence.\nNote that this field cannot be set when spec.os.name is windows."

## obj spec.containers.securityContext.capabilities

"The capabilities to add/drop when running containers.\nDefaults to the default set of capabilities granted by the container runtime.\nNote that this field cannot be set when spec.os.name is windows."

### fn spec.containers.securityContext.capabilities.withAdd

```ts
withAdd(add)
```

"This is accessible behind a feature flag - kubernetes.containerspec-addcapabilities"

### fn spec.containers.securityContext.capabilities.withAddMixin

```ts
withAddMixin(add)
```

"This is accessible behind a feature flag - kubernetes.containerspec-addcapabilities"

**Note:** This function appends passed data to existing values

### fn spec.containers.securityContext.capabilities.withDrop

```ts
withDrop(drop)
```

"Removed capabilities"

### fn spec.containers.securityContext.capabilities.withDropMixin

```ts
withDropMixin(drop)
```

"Removed capabilities"

**Note:** This function appends passed data to existing values

## obj spec.containers.securityContext.seccompProfile

"The seccomp options to use by this container. If seccomp options are\nprovided at both the pod & container level, the container options\noverride the pod options.\nNote that this field cannot be set when spec.os.name is windows."

### fn spec.containers.securityContext.seccompProfile.withLocalhostProfile

```ts
withLocalhostProfile(localhostProfile)
```

"localhostProfile indicates a profile defined in a file on the node should be used.\nThe profile must be preconfigured on the node to work.\nMust be a descending path, relative to the kubelet's configured seccomp profile location.\nMust be set if type is \"Localhost\". Must NOT be set for any other type."

### fn spec.containers.securityContext.seccompProfile.withType

```ts
withType(type)
```

"type indicates which kind of seccomp profile will be applied.\nValid options are:\n\n\nLocalhost - a profile defined in a file on the node should be used.\nRuntimeDefault - the container runtime default profile should be used.\nUnconfined - no profile should be applied."

## obj spec.containers.startupProbe

"StartupProbe indicates that the Pod has successfully initialized.\nIf specified, no other probes are executed until this completes successfully.\nIf this probe fails, the Pod will be restarted, just as if the livenessProbe failed.\nThis can be used to provide different probe parameters at the beginning of a Pod's lifecycle,\nwhen it might take a long time to load data or warm a cache, than during steady-state operation.\nThis cannot be updated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.containers.startupProbe.withFailureThreshold

```ts
withFailureThreshold(failureThreshold)
```

"Minimum consecutive failures for the probe to be considered failed after having succeeded.\nDefaults to 3. Minimum value is 1."

### fn spec.containers.startupProbe.withInitialDelaySeconds

```ts
withInitialDelaySeconds(initialDelaySeconds)
```

"Number of seconds after the container has started before liveness probes are initiated.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.containers.startupProbe.withPeriodSeconds

```ts
withPeriodSeconds(periodSeconds)
```

"How often (in seconds) to perform the probe."

### fn spec.containers.startupProbe.withSuccessThreshold

```ts
withSuccessThreshold(successThreshold)
```

"Minimum consecutive successes for the probe to be considered successful after having failed.\nDefaults to 1. Must be 1 for liveness and startup. Minimum value is 1."

### fn spec.containers.startupProbe.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"Number of seconds after which the probe times out.\nDefaults to 1 second. Minimum value is 1.\nMore info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

## obj spec.containers.startupProbe.exec

"Exec specifies the action to take."

### fn spec.containers.startupProbe.exec.withCommand

```ts
withCommand(command)
```

"Command is the command line to execute inside the container, the working directory for the\ncommand  is root ('/') in the container's filesystem. The command is simply exec'd, it is\nnot run inside a shell, so traditional shell instructions ('|', etc) won't work. To use\na shell, you need to explicitly call out to that shell.\nExit status of 0 is treated as live/healthy and non-zero is unhealthy."

### fn spec.containers.startupProbe.exec.withCommandMixin

```ts
withCommandMixin(command)
```

"Command is the command line to execute inside the container, the working directory for the\ncommand  is root ('/') in the container's filesystem. The command is simply exec'd, it is\nnot run inside a shell, so traditional shell instructions ('|', etc) won't work. To use\na shell, you need to explicitly call out to that shell.\nExit status of 0 is treated as live/healthy and non-zero is unhealthy."

**Note:** This function appends passed data to existing values

## obj spec.containers.startupProbe.grpc

"GRPC specifies an action involving a GRPC port."

### fn spec.containers.startupProbe.grpc.withPort

```ts
withPort(port)
```

"Port number of the gRPC service. Number must be in the range 1 to 65535."

### fn spec.containers.startupProbe.grpc.withService

```ts
withService(service)
```

"Service is the name of the service to place in the gRPC HealthCheckRequest\n(see https://github.com/grpc/grpc/blob/master/doc/health-checking.md).\n\n\nIf this is not specified, the default behavior is defined by gRPC."

## obj spec.containers.startupProbe.httpGet

"HTTPGet specifies the http request to perform."

### fn spec.containers.startupProbe.httpGet.withHost

```ts
withHost(host)
```

"Host name to connect to, defaults to the pod IP. You probably want to set\n\"Host\" in httpHeaders instead."

### fn spec.containers.startupProbe.httpGet.withHttpHeaders

```ts
withHttpHeaders(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.containers.startupProbe.httpGet.withHttpHeadersMixin

```ts
withHttpHeadersMixin(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

**Note:** This function appends passed data to existing values

### fn spec.containers.startupProbe.httpGet.withPath

```ts
withPath(path)
```

"Path to access on the HTTP server."

### fn spec.containers.startupProbe.httpGet.withPort

```ts
withPort(port)
```

"Name or number of the port to access on the container.\nNumber must be in the range 1 to 65535.\nName must be an IANA_SVC_NAME."

### fn spec.containers.startupProbe.httpGet.withScheme

```ts
withScheme(scheme)
```

"Scheme to use for connecting to the host.\nDefaults to HTTP."

## obj spec.containers.startupProbe.httpGet.httpHeaders

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.containers.startupProbe.httpGet.httpHeaders.withName

```ts
withName(name)
```

"The header field name.\nThis will be canonicalized upon output, so case-variant names will be understood as the same header."

### fn spec.containers.startupProbe.httpGet.httpHeaders.withValue

```ts
withValue(value)
```

"The header field value"

## obj spec.containers.startupProbe.tcpSocket

"TCPSocket specifies an action involving a TCP port."

### fn spec.containers.startupProbe.tcpSocket.withHost

```ts
withHost(host)
```

"Optional: Host name to connect to, defaults to the pod IP."

### fn spec.containers.startupProbe.tcpSocket.withPort

```ts
withPort(port)
```

"Number or name of the port to access on the container.\nNumber must be in the range 1 to 65535.\nName must be an IANA_SVC_NAME."

## obj spec.containers.volumeMounts

"Pod volumes to mount into the container's filesystem.\nCannot be updated."

### fn spec.containers.volumeMounts.withMountPath

```ts
withMountPath(mountPath)
```

"Path within the container at which the volume should be mounted.  Must\nnot contain ':'."

### fn spec.containers.volumeMounts.withName

```ts
withName(name)
```

"This must match the Name of a Volume."

### fn spec.containers.volumeMounts.withReadOnly

```ts
withReadOnly(readOnly)
```

"Mounted read-only if true, read-write otherwise (false or unspecified).\nDefaults to false."

### fn spec.containers.volumeMounts.withSubPath

```ts
withSubPath(subPath)
```

"Path within the volume from which the container's volume should be mounted.\nDefaults to \"\" (volume's root)."

## obj spec.imagePullSecrets

"ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec.\nIf specified, these secrets will be passed to individual puller implementations for them to use.\nMore info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod"

### fn spec.imagePullSecrets.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

## obj spec.volumes

"List of volumes that can be mounted by containers belonging to the pod.\nMore info: https://kubernetes.io/docs/concepts/storage/volumes"

### fn spec.volumes.withEmptyDir

```ts
withEmptyDir(emptyDir)
```

"This is accessible behind a feature flag - kubernetes.podspec-emptydir"

### fn spec.volumes.withEmptyDirMixin

```ts
withEmptyDirMixin(emptyDir)
```

"This is accessible behind a feature flag - kubernetes.podspec-emptydir"

**Note:** This function appends passed data to existing values

### fn spec.volumes.withName

```ts
withName(name)
```

"name of the volume.\nMust be a DNS_LABEL and unique within the pod.\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names"

### fn spec.volumes.withPersistentVolumeClaim

```ts
withPersistentVolumeClaim(persistentVolumeClaim)
```

"This is accessible behind a feature flag - kubernetes.podspec-persistent-volume-claim"

### fn spec.volumes.withPersistentVolumeClaimMixin

```ts
withPersistentVolumeClaimMixin(persistentVolumeClaim)
```

"This is accessible behind a feature flag - kubernetes.podspec-persistent-volume-claim"

**Note:** This function appends passed data to existing values

## obj spec.volumes.configMap

"configMap represents a configMap that should populate this volume"

### fn spec.volumes.configMap.withDefaultMode

```ts
withDefaultMode(defaultMode)
```

"defaultMode is optional: mode bits used to set permissions on created files by default.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nDefaults to 0644.\nDirectories within the path are not affected by this setting.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.configMap.withItems

```ts
withItems(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced\nConfigMap will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the ConfigMap,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.configMap.withItemsMixin

```ts
withItemsMixin(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced\nConfigMap will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the ConfigMap,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.volumes.configMap.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.volumes.configMap.withOptional

```ts
withOptional(optional)
```

"optional specify whether the ConfigMap or its keys must be defined"

## obj spec.volumes.configMap.items

"items if unspecified, each key-value pair in the Data field of the referenced\nConfigMap will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the ConfigMap,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.configMap.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.volumes.configMap.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nIf not specified, the volume defaultMode will be used.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.configMap.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to.\nMay not be an absolute path.\nMay not contain the path element '..'.\nMay not start with the string '..'."

## obj spec.volumes.projected

"projected items for all in one resources secrets, configmaps, and downward API"

### fn spec.volumes.projected.withDefaultMode

```ts
withDefaultMode(defaultMode)
```

"defaultMode are the mode bits used to set permissions on created files by default.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nDirectories within the path are not affected by this setting.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.projected.withSources

```ts
withSources(sources)
```

"sources is the list of volume projections"

### fn spec.volumes.projected.withSourcesMixin

```ts
withSourcesMixin(sources)
```

"sources is the list of volume projections"

**Note:** This function appends passed data to existing values

## obj spec.volumes.projected.sources

"sources is the list of volume projections"

## obj spec.volumes.projected.sources.configMap

"configMap information about the configMap data to project"

### fn spec.volumes.projected.sources.configMap.withItems

```ts
withItems(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced\nConfigMap will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the ConfigMap,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.projected.sources.configMap.withItemsMixin

```ts
withItemsMixin(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced\nConfigMap will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the ConfigMap,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.volumes.projected.sources.configMap.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.volumes.projected.sources.configMap.withOptional

```ts
withOptional(optional)
```

"optional specify whether the ConfigMap or its keys must be defined"

## obj spec.volumes.projected.sources.configMap.items

"items if unspecified, each key-value pair in the Data field of the referenced\nConfigMap will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the ConfigMap,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.projected.sources.configMap.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.volumes.projected.sources.configMap.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nIf not specified, the volume defaultMode will be used.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.projected.sources.configMap.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to.\nMay not be an absolute path.\nMay not contain the path element '..'.\nMay not start with the string '..'."

## obj spec.volumes.projected.sources.downwardAPI

"downwardAPI information about the downwardAPI data to project"

### fn spec.volumes.projected.sources.downwardAPI.withItems

```ts
withItems(items)
```

"Items is a list of DownwardAPIVolume file"

### fn spec.volumes.projected.sources.downwardAPI.withItemsMixin

```ts
withItemsMixin(items)
```

"Items is a list of DownwardAPIVolume file"

**Note:** This function appends passed data to existing values

## obj spec.volumes.projected.sources.downwardAPI.items

"Items is a list of DownwardAPIVolume file"

### fn spec.volumes.projected.sources.downwardAPI.items.withMode

```ts
withMode(mode)
```

"Optional: mode bits used to set permissions on this file, must be an octal value\nbetween 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nIf not specified, the volume defaultMode will be used.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.projected.sources.downwardAPI.items.withPath

```ts
withPath(path)
```

"Required: Path is  the relative path name of the file to be created. Must not be absolute or contain the '..' path. Must be utf-8 encoded. The first item of the relative path must not start with '..'"

## obj spec.volumes.projected.sources.downwardAPI.items.fieldRef

"Required: Selects a field of the pod: only annotations, labels, name, namespace and uid are supported."

### fn spec.volumes.projected.sources.downwardAPI.items.fieldRef.withApiVersion

```ts
withApiVersion(apiVersion)
```

"Version of the schema the FieldPath is written in terms of, defaults to \"v1\"."

### fn spec.volumes.projected.sources.downwardAPI.items.fieldRef.withFieldPath

```ts
withFieldPath(fieldPath)
```

"Path of the field to select in the specified API version."

## obj spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef

"Selects a resource of the container: only resources limits and requests\n(limits.cpu, limits.memory, requests.cpu and requests.memory) are currently supported."

### fn spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef.withContainerName

```ts
withContainerName(containerName)
```

"Container name: required for volumes, optional for env vars"

### fn spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef.withDivisor

```ts
withDivisor(divisor)
```

"Specifies the output format of the exposed resources, defaults to \"1\

### fn spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef.withResource

```ts
withResource(resource)
```

"Required: resource to select"

## obj spec.volumes.projected.sources.secret

"secret information about the secret data to project"

### fn spec.volumes.projected.sources.secret.withItems

```ts
withItems(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced\nSecret will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the Secret,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.projected.sources.secret.withItemsMixin

```ts
withItemsMixin(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced\nSecret will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the Secret,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.volumes.projected.sources.secret.withName

```ts
withName(name)
```

"Name of the referent.\nThis field is effectively required, but due to backwards compatibility is\nallowed to be empty. Instances of this type with an empty value here are\nalmost certainly wrong.\nTODO: Add other useful fields. apiVersion, kind, uid?\nMore info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names\nTODO: Drop `kubebuilder:default` when controller-gen doesn't need it https://github.com/kubernetes-sigs/kubebuilder/issues/3896."

### fn spec.volumes.projected.sources.secret.withOptional

```ts
withOptional(optional)
```

"optional field specify whether the Secret or its key must be defined"

## obj spec.volumes.projected.sources.secret.items

"items if unspecified, each key-value pair in the Data field of the referenced\nSecret will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the Secret,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.projected.sources.secret.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.volumes.projected.sources.secret.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nIf not specified, the volume defaultMode will be used.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.projected.sources.secret.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to.\nMay not be an absolute path.\nMay not contain the path element '..'.\nMay not start with the string '..'."

## obj spec.volumes.projected.sources.serviceAccountToken

"serviceAccountToken is information about the serviceAccountToken data to project"

### fn spec.volumes.projected.sources.serviceAccountToken.withAudience

```ts
withAudience(audience)
```

"audience is the intended audience of the token. A recipient of a token\nmust identify itself with an identifier specified in the audience of the\ntoken, and otherwise should reject the token. The audience defaults to the\nidentifier of the apiserver."

### fn spec.volumes.projected.sources.serviceAccountToken.withExpirationSeconds

```ts
withExpirationSeconds(expirationSeconds)
```

"expirationSeconds is the requested duration of validity of the service\naccount token. As the token approaches expiration, the kubelet volume\nplugin will proactively rotate the service account token. The kubelet will\nstart trying to rotate the token if the token is older than 80 percent of\nits time to live or if the token is older than 24 hours.Defaults to 1 hour\nand must be at least 10 minutes."

### fn spec.volumes.projected.sources.serviceAccountToken.withPath

```ts
withPath(path)
```

"path is the path relative to the mount point of the file to project the\ntoken into."

## obj spec.volumes.secret

"secret represents a secret that should populate this volume.\nMore info: https://kubernetes.io/docs/concepts/storage/volumes#secret"

### fn spec.volumes.secret.withDefaultMode

```ts
withDefaultMode(defaultMode)
```

"defaultMode is Optional: mode bits used to set permissions on created files by default.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values\nfor mode bits. Defaults to 0644.\nDirectories within the path are not affected by this setting.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.secret.withItems

```ts
withItems(items)
```

"items If unspecified, each key-value pair in the Data field of the referenced\nSecret will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the Secret,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.secret.withItemsMixin

```ts
withItemsMixin(items)
```

"items If unspecified, each key-value pair in the Data field of the referenced\nSecret will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the Secret,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.volumes.secret.withOptional

```ts
withOptional(optional)
```

"optional field specify whether the Secret or its keys must be defined"

### fn spec.volumes.secret.withSecretName

```ts
withSecretName(secretName)
```

"secretName is the name of the secret in the pod's namespace to use.\nMore info: https://kubernetes.io/docs/concepts/storage/volumes#secret"

## obj spec.volumes.secret.items

"items If unspecified, each key-value pair in the Data field of the referenced\nSecret will be projected into the volume as a file whose name is the\nkey and content is the value. If specified, the listed keys will be\nprojected into the specified paths, and unlisted keys will not be\npresent. If a key is specified which is not present in the Secret,\nthe volume setup will error unless it is marked optional. Paths must be\nrelative and may not contain the '..' path or start with '..'."

### fn spec.volumes.secret.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.volumes.secret.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file.\nMust be an octal value between 0000 and 0777 or a decimal value between 0 and 511.\nYAML accepts both octal and decimal values, JSON requires decimal values for mode bits.\nIf not specified, the volume defaultMode will be used.\nThis might be in conflict with other options that affect the file\nmode, like fsGroup, and the result can be other mode bits set."

### fn spec.volumes.secret.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to.\nMay not be an absolute path.\nMay not contain the path element '..'.\nMay not start with the string '..'."