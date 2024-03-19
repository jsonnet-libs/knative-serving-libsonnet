---
permalink: /1.12.3/serving/v1/service/
---

# serving.v1.service

"Service acts as a top-level container that manages a Route and Configuration which implement a network service. Service exists to provide a singular abstraction which can be access controlled, reasoned about, and which encapsulates software lifecycle decisions such as rollout policy and team resource ownership. Service acts only as an orchestrator of the underlying Routes and Configurations (much as a kubernetes Deployment orchestrates ReplicaSets), and its usage is optional but recommended. \n The Service's controller will track the statuses of its owned Configuration and Route, reflecting their statuses and conditions as its own. \n See also: https://github.com/knative/serving/blob/main/docs/spec/overview.md#service"

## Index

* [`fn new(name)`](#fn-new)
* [`fn mapContainers(f)`](#fn-mapcontainers)
* [`fn mapContainersWithName(names, f)`](#fn-mapcontainerswithname)
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
  * [`fn withTraffic(traffic)`](#fn-specwithtraffic)
  * [`fn withTrafficMixin(traffic)`](#fn-specwithtrafficmixin)
  * [`obj spec.template`](#obj-spectemplate)
    * [`obj spec.template.metadata`](#obj-spectemplatemetadata)
      * [`fn withAnnotations(annotations)`](#fn-spectemplatemetadatawithannotations)
      * [`fn withAnnotationsMixin(annotations)`](#fn-spectemplatemetadatawithannotationsmixin)
      * [`fn withFinalizers(finalizers)`](#fn-spectemplatemetadatawithfinalizers)
      * [`fn withFinalizersMixin(finalizers)`](#fn-spectemplatemetadatawithfinalizersmixin)
      * [`fn withLabels(labels)`](#fn-spectemplatemetadatawithlabels)
      * [`fn withLabelsMixin(labels)`](#fn-spectemplatemetadatawithlabelsmixin)
      * [`fn withName(name)`](#fn-spectemplatemetadatawithname)
      * [`fn withNamespace(namespace)`](#fn-spectemplatemetadatawithnamespace)
    * [`obj spec.template.spec`](#obj-spectemplatespec)
      * [`fn withAffinity(affinity)`](#fn-spectemplatespecwithaffinity)
      * [`fn withAffinityMixin(affinity)`](#fn-spectemplatespecwithaffinitymixin)
      * [`fn withAutomountServiceAccountToken(automountServiceAccountToken)`](#fn-spectemplatespecwithautomountserviceaccounttoken)
      * [`fn withContainerConcurrency(containerConcurrency)`](#fn-spectemplatespecwithcontainerconcurrency)
      * [`fn withContainers(containers)`](#fn-spectemplatespecwithcontainers)
      * [`fn withContainersMixin(containers)`](#fn-spectemplatespecwithcontainersmixin)
      * [`fn withDnsConfig(dnsConfig)`](#fn-spectemplatespecwithdnsconfig)
      * [`fn withDnsConfigMixin(dnsConfig)`](#fn-spectemplatespecwithdnsconfigmixin)
      * [`fn withDnsPolicy(dnsPolicy)`](#fn-spectemplatespecwithdnspolicy)
      * [`fn withEnableServiceLinks(enableServiceLinks)`](#fn-spectemplatespecwithenableservicelinks)
      * [`fn withHostAliases(hostAliases)`](#fn-spectemplatespecwithhostaliases)
      * [`fn withHostAliasesMixin(hostAliases)`](#fn-spectemplatespecwithhostaliasesmixin)
      * [`fn withIdleTimeoutSeconds(idleTimeoutSeconds)`](#fn-spectemplatespecwithidletimeoutseconds)
      * [`fn withImagePullSecrets(imagePullSecrets)`](#fn-spectemplatespecwithimagepullsecrets)
      * [`fn withImagePullSecretsMixin(imagePullSecrets)`](#fn-spectemplatespecwithimagepullsecretsmixin)
      * [`fn withInitContainers(initContainers)`](#fn-spectemplatespecwithinitcontainers)
      * [`fn withInitContainersMixin(initContainers)`](#fn-spectemplatespecwithinitcontainersmixin)
      * [`fn withNodeSelector(nodeSelector)`](#fn-spectemplatespecwithnodeselector)
      * [`fn withNodeSelectorMixin(nodeSelector)`](#fn-spectemplatespecwithnodeselectormixin)
      * [`fn withPriorityClassName(priorityClassName)`](#fn-spectemplatespecwithpriorityclassname)
      * [`fn withResponseStartTimeoutSeconds(responseStartTimeoutSeconds)`](#fn-spectemplatespecwithresponsestarttimeoutseconds)
      * [`fn withRuntimeClassName(runtimeClassName)`](#fn-spectemplatespecwithruntimeclassname)
      * [`fn withSchedulerName(schedulerName)`](#fn-spectemplatespecwithschedulername)
      * [`fn withSecurityContext(securityContext)`](#fn-spectemplatespecwithsecuritycontext)
      * [`fn withSecurityContextMixin(securityContext)`](#fn-spectemplatespecwithsecuritycontextmixin)
      * [`fn withServiceAccountName(serviceAccountName)`](#fn-spectemplatespecwithserviceaccountname)
      * [`fn withShareProcessNamespace(shareProcessNamespace)`](#fn-spectemplatespecwithshareprocessnamespace)
      * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-spectemplatespecwithtimeoutseconds)
      * [`fn withTolerations(tolerations)`](#fn-spectemplatespecwithtolerations)
      * [`fn withTolerationsMixin(tolerations)`](#fn-spectemplatespecwithtolerationsmixin)
      * [`fn withTopologySpreadConstraints(topologySpreadConstraints)`](#fn-spectemplatespecwithtopologyspreadconstraints)
      * [`fn withTopologySpreadConstraintsMixin(topologySpreadConstraints)`](#fn-spectemplatespecwithtopologyspreadconstraintsmixin)
      * [`fn withVolumes(volumes)`](#fn-spectemplatespecwithvolumes)
      * [`fn withVolumesMixin(volumes)`](#fn-spectemplatespecwithvolumesmixin)
      * [`obj spec.template.spec.containers`](#obj-spectemplatespeccontainers)
        * [`fn withArgs(args)`](#fn-spectemplatespeccontainerswithargs)
        * [`fn withArgsMixin(args)`](#fn-spectemplatespeccontainerswithargsmixin)
        * [`fn withCommand(command)`](#fn-spectemplatespeccontainerswithcommand)
        * [`fn withCommandMixin(command)`](#fn-spectemplatespeccontainerswithcommandmixin)
        * [`fn withEnv(env)`](#fn-spectemplatespeccontainerswithenv)
        * [`fn withEnvFrom(envFrom)`](#fn-spectemplatespeccontainerswithenvfrom)
        * [`fn withEnvFromMixin(envFrom)`](#fn-spectemplatespeccontainerswithenvfrommixin)
        * [`fn withEnvMixin(env)`](#fn-spectemplatespeccontainerswithenvmixin)
        * [`fn withImage(image)`](#fn-spectemplatespeccontainerswithimage)
        * [`fn withImagePullPolicy(imagePullPolicy)`](#fn-spectemplatespeccontainerswithimagepullpolicy)
        * [`fn withName(name)`](#fn-spectemplatespeccontainerswithname)
        * [`fn withPorts(ports)`](#fn-spectemplatespeccontainerswithports)
        * [`fn withPortsMixin(ports)`](#fn-spectemplatespeccontainerswithportsmixin)
        * [`fn withTerminationMessagePath(terminationMessagePath)`](#fn-spectemplatespeccontainerswithterminationmessagepath)
        * [`fn withTerminationMessagePolicy(terminationMessagePolicy)`](#fn-spectemplatespeccontainerswithterminationmessagepolicy)
        * [`fn withVolumeMounts(volumeMounts)`](#fn-spectemplatespeccontainerswithvolumemounts)
        * [`fn withVolumeMountsMixin(volumeMounts)`](#fn-spectemplatespeccontainerswithvolumemountsmixin)
        * [`fn withWorkingDir(workingDir)`](#fn-spectemplatespeccontainerswithworkingdir)
        * [`obj spec.template.spec.containers.env`](#obj-spectemplatespeccontainersenv)
          * [`fn withName(name)`](#fn-spectemplatespeccontainersenvwithname)
          * [`fn withValue(value)`](#fn-spectemplatespeccontainersenvwithvalue)
          * [`obj spec.template.spec.containers.env.valueFrom`](#obj-spectemplatespeccontainersenvvaluefrom)
            * [`fn withFieldRef(fieldRef)`](#fn-spectemplatespeccontainersenvvaluefromwithfieldref)
            * [`fn withFieldRefMixin(fieldRef)`](#fn-spectemplatespeccontainersenvvaluefromwithfieldrefmixin)
            * [`fn withResourceFieldRef(resourceFieldRef)`](#fn-spectemplatespeccontainersenvvaluefromwithresourcefieldref)
            * [`fn withResourceFieldRefMixin(resourceFieldRef)`](#fn-spectemplatespeccontainersenvvaluefromwithresourcefieldrefmixin)
            * [`obj spec.template.spec.containers.env.valueFrom.configMapKeyRef`](#obj-spectemplatespeccontainersenvvaluefromconfigmapkeyref)
              * [`fn withKey(key)`](#fn-spectemplatespeccontainersenvvaluefromconfigmapkeyrefwithkey)
              * [`fn withName(name)`](#fn-spectemplatespeccontainersenvvaluefromconfigmapkeyrefwithname)
              * [`fn withOptional(optional)`](#fn-spectemplatespeccontainersenvvaluefromconfigmapkeyrefwithoptional)
            * [`obj spec.template.spec.containers.env.valueFrom.secretKeyRef`](#obj-spectemplatespeccontainersenvvaluefromsecretkeyref)
              * [`fn withKey(key)`](#fn-spectemplatespeccontainersenvvaluefromsecretkeyrefwithkey)
              * [`fn withName(name)`](#fn-spectemplatespeccontainersenvvaluefromsecretkeyrefwithname)
              * [`fn withOptional(optional)`](#fn-spectemplatespeccontainersenvvaluefromsecretkeyrefwithoptional)
        * [`obj spec.template.spec.containers.envFrom`](#obj-spectemplatespeccontainersenvfrom)
          * [`fn withPrefix(prefix)`](#fn-spectemplatespeccontainersenvfromwithprefix)
          * [`obj spec.template.spec.containers.envFrom.configMapRef`](#obj-spectemplatespeccontainersenvfromconfigmapref)
            * [`fn withName(name)`](#fn-spectemplatespeccontainersenvfromconfigmaprefwithname)
            * [`fn withOptional(optional)`](#fn-spectemplatespeccontainersenvfromconfigmaprefwithoptional)
          * [`obj spec.template.spec.containers.envFrom.secretRef`](#obj-spectemplatespeccontainersenvfromsecretref)
            * [`fn withName(name)`](#fn-spectemplatespeccontainersenvfromsecretrefwithname)
            * [`fn withOptional(optional)`](#fn-spectemplatespeccontainersenvfromsecretrefwithoptional)
        * [`obj spec.template.spec.containers.livenessProbe`](#obj-spectemplatespeccontainerslivenessprobe)
          * [`fn withFailureThreshold(failureThreshold)`](#fn-spectemplatespeccontainerslivenessprobewithfailurethreshold)
          * [`fn withInitialDelaySeconds(initialDelaySeconds)`](#fn-spectemplatespeccontainerslivenessprobewithinitialdelayseconds)
          * [`fn withPeriodSeconds(periodSeconds)`](#fn-spectemplatespeccontainerslivenessprobewithperiodseconds)
          * [`fn withSuccessThreshold(successThreshold)`](#fn-spectemplatespeccontainerslivenessprobewithsuccessthreshold)
          * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-spectemplatespeccontainerslivenessprobewithtimeoutseconds)
          * [`obj spec.template.spec.containers.livenessProbe.exec`](#obj-spectemplatespeccontainerslivenessprobeexec)
            * [`fn withCommand(command)`](#fn-spectemplatespeccontainerslivenessprobeexecwithcommand)
            * [`fn withCommandMixin(command)`](#fn-spectemplatespeccontainerslivenessprobeexecwithcommandmixin)
          * [`obj spec.template.spec.containers.livenessProbe.grpc`](#obj-spectemplatespeccontainerslivenessprobegrpc)
            * [`fn withPort(port)`](#fn-spectemplatespeccontainerslivenessprobegrpcwithport)
            * [`fn withService(service)`](#fn-spectemplatespeccontainerslivenessprobegrpcwithservice)
          * [`obj spec.template.spec.containers.livenessProbe.httpGet`](#obj-spectemplatespeccontainerslivenessprobehttpget)
            * [`fn withHost(host)`](#fn-spectemplatespeccontainerslivenessprobehttpgetwithhost)
            * [`fn withHttpHeaders(httpHeaders)`](#fn-spectemplatespeccontainerslivenessprobehttpgetwithhttpheaders)
            * [`fn withHttpHeadersMixin(httpHeaders)`](#fn-spectemplatespeccontainerslivenessprobehttpgetwithhttpheadersmixin)
            * [`fn withPath(path)`](#fn-spectemplatespeccontainerslivenessprobehttpgetwithpath)
            * [`fn withPort(port)`](#fn-spectemplatespeccontainerslivenessprobehttpgetwithport)
            * [`fn withScheme(scheme)`](#fn-spectemplatespeccontainerslivenessprobehttpgetwithscheme)
            * [`obj spec.template.spec.containers.livenessProbe.httpGet.httpHeaders`](#obj-spectemplatespeccontainerslivenessprobehttpgethttpheaders)
              * [`fn withName(name)`](#fn-spectemplatespeccontainerslivenessprobehttpgethttpheaderswithname)
              * [`fn withValue(value)`](#fn-spectemplatespeccontainerslivenessprobehttpgethttpheaderswithvalue)
          * [`obj spec.template.spec.containers.livenessProbe.tcpSocket`](#obj-spectemplatespeccontainerslivenessprobetcpsocket)
            * [`fn withHost(host)`](#fn-spectemplatespeccontainerslivenessprobetcpsocketwithhost)
            * [`fn withPort(port)`](#fn-spectemplatespeccontainerslivenessprobetcpsocketwithport)
        * [`obj spec.template.spec.containers.ports`](#obj-spectemplatespeccontainersports)
          * [`fn withContainerPort(containerPort)`](#fn-spectemplatespeccontainersportswithcontainerport)
          * [`fn withName(name)`](#fn-spectemplatespeccontainersportswithname)
          * [`fn withProtocol(protocol)`](#fn-spectemplatespeccontainersportswithprotocol)
        * [`obj spec.template.spec.containers.readinessProbe`](#obj-spectemplatespeccontainersreadinessprobe)
          * [`fn withFailureThreshold(failureThreshold)`](#fn-spectemplatespeccontainersreadinessprobewithfailurethreshold)
          * [`fn withInitialDelaySeconds(initialDelaySeconds)`](#fn-spectemplatespeccontainersreadinessprobewithinitialdelayseconds)
          * [`fn withPeriodSeconds(periodSeconds)`](#fn-spectemplatespeccontainersreadinessprobewithperiodseconds)
          * [`fn withSuccessThreshold(successThreshold)`](#fn-spectemplatespeccontainersreadinessprobewithsuccessthreshold)
          * [`fn withTimeoutSeconds(timeoutSeconds)`](#fn-spectemplatespeccontainersreadinessprobewithtimeoutseconds)
          * [`obj spec.template.spec.containers.readinessProbe.exec`](#obj-spectemplatespeccontainersreadinessprobeexec)
            * [`fn withCommand(command)`](#fn-spectemplatespeccontainersreadinessprobeexecwithcommand)
            * [`fn withCommandMixin(command)`](#fn-spectemplatespeccontainersreadinessprobeexecwithcommandmixin)
          * [`obj spec.template.spec.containers.readinessProbe.grpc`](#obj-spectemplatespeccontainersreadinessprobegrpc)
            * [`fn withPort(port)`](#fn-spectemplatespeccontainersreadinessprobegrpcwithport)
            * [`fn withService(service)`](#fn-spectemplatespeccontainersreadinessprobegrpcwithservice)
          * [`obj spec.template.spec.containers.readinessProbe.httpGet`](#obj-spectemplatespeccontainersreadinessprobehttpget)
            * [`fn withHost(host)`](#fn-spectemplatespeccontainersreadinessprobehttpgetwithhost)
            * [`fn withHttpHeaders(httpHeaders)`](#fn-spectemplatespeccontainersreadinessprobehttpgetwithhttpheaders)
            * [`fn withHttpHeadersMixin(httpHeaders)`](#fn-spectemplatespeccontainersreadinessprobehttpgetwithhttpheadersmixin)
            * [`fn withPath(path)`](#fn-spectemplatespeccontainersreadinessprobehttpgetwithpath)
            * [`fn withPort(port)`](#fn-spectemplatespeccontainersreadinessprobehttpgetwithport)
            * [`fn withScheme(scheme)`](#fn-spectemplatespeccontainersreadinessprobehttpgetwithscheme)
            * [`obj spec.template.spec.containers.readinessProbe.httpGet.httpHeaders`](#obj-spectemplatespeccontainersreadinessprobehttpgethttpheaders)
              * [`fn withName(name)`](#fn-spectemplatespeccontainersreadinessprobehttpgethttpheaderswithname)
              * [`fn withValue(value)`](#fn-spectemplatespeccontainersreadinessprobehttpgethttpheaderswithvalue)
          * [`obj spec.template.spec.containers.readinessProbe.tcpSocket`](#obj-spectemplatespeccontainersreadinessprobetcpsocket)
            * [`fn withHost(host)`](#fn-spectemplatespeccontainersreadinessprobetcpsocketwithhost)
            * [`fn withPort(port)`](#fn-spectemplatespeccontainersreadinessprobetcpsocketwithport)
        * [`obj spec.template.spec.containers.resources`](#obj-spectemplatespeccontainersresources)
          * [`fn withClaims(claims)`](#fn-spectemplatespeccontainersresourceswithclaims)
          * [`fn withClaimsMixin(claims)`](#fn-spectemplatespeccontainersresourceswithclaimsmixin)
          * [`fn withLimits(limits)`](#fn-spectemplatespeccontainersresourceswithlimits)
          * [`fn withLimitsMixin(limits)`](#fn-spectemplatespeccontainersresourceswithlimitsmixin)
          * [`fn withRequests(requests)`](#fn-spectemplatespeccontainersresourceswithrequests)
          * [`fn withRequestsMixin(requests)`](#fn-spectemplatespeccontainersresourceswithrequestsmixin)
          * [`obj spec.template.spec.containers.resources.claims`](#obj-spectemplatespeccontainersresourcesclaims)
            * [`fn withName(name)`](#fn-spectemplatespeccontainersresourcesclaimswithname)
        * [`obj spec.template.spec.containers.securityContext`](#obj-spectemplatespeccontainerssecuritycontext)
          * [`fn withAllowPrivilegeEscalation(allowPrivilegeEscalation)`](#fn-spectemplatespeccontainerssecuritycontextwithallowprivilegeescalation)
          * [`fn withReadOnlyRootFilesystem(readOnlyRootFilesystem)`](#fn-spectemplatespeccontainerssecuritycontextwithreadonlyrootfilesystem)
          * [`fn withRunAsGroup(runAsGroup)`](#fn-spectemplatespeccontainerssecuritycontextwithrunasgroup)
          * [`fn withRunAsNonRoot(runAsNonRoot)`](#fn-spectemplatespeccontainerssecuritycontextwithrunasnonroot)
          * [`fn withRunAsUser(runAsUser)`](#fn-spectemplatespeccontainerssecuritycontextwithrunasuser)
          * [`obj spec.template.spec.containers.securityContext.capabilities`](#obj-spectemplatespeccontainerssecuritycontextcapabilities)
            * [`fn withAdd(add)`](#fn-spectemplatespeccontainerssecuritycontextcapabilitieswithadd)
            * [`fn withAddMixin(add)`](#fn-spectemplatespeccontainerssecuritycontextcapabilitieswithaddmixin)
            * [`fn withDrop(drop)`](#fn-spectemplatespeccontainerssecuritycontextcapabilitieswithdrop)
            * [`fn withDropMixin(drop)`](#fn-spectemplatespeccontainerssecuritycontextcapabilitieswithdropmixin)
          * [`obj spec.template.spec.containers.securityContext.seccompProfile`](#obj-spectemplatespeccontainerssecuritycontextseccompprofile)
            * [`fn withLocalhostProfile(localhostProfile)`](#fn-spectemplatespeccontainerssecuritycontextseccompprofilewithlocalhostprofile)
            * [`fn withType(type)`](#fn-spectemplatespeccontainerssecuritycontextseccompprofilewithtype)
        * [`obj spec.template.spec.containers.volumeMounts`](#obj-spectemplatespeccontainersvolumemounts)
          * [`fn withMountPath(mountPath)`](#fn-spectemplatespeccontainersvolumemountswithmountpath)
          * [`fn withName(name)`](#fn-spectemplatespeccontainersvolumemountswithname)
          * [`fn withReadOnly(readOnly)`](#fn-spectemplatespeccontainersvolumemountswithreadonly)
          * [`fn withSubPath(subPath)`](#fn-spectemplatespeccontainersvolumemountswithsubpath)
      * [`obj spec.template.spec.imagePullSecrets`](#obj-spectemplatespecimagepullsecrets)
        * [`fn withName(name)`](#fn-spectemplatespecimagepullsecretswithname)
      * [`obj spec.template.spec.volumes`](#obj-spectemplatespecvolumes)
        * [`fn withEmptyDir(emptyDir)`](#fn-spectemplatespecvolumeswithemptydir)
        * [`fn withEmptyDirMixin(emptyDir)`](#fn-spectemplatespecvolumeswithemptydirmixin)
        * [`fn withName(name)`](#fn-spectemplatespecvolumeswithname)
        * [`fn withPersistentVolumeClaim(persistentVolumeClaim)`](#fn-spectemplatespecvolumeswithpersistentvolumeclaim)
        * [`fn withPersistentVolumeClaimMixin(persistentVolumeClaim)`](#fn-spectemplatespecvolumeswithpersistentvolumeclaimmixin)
        * [`obj spec.template.spec.volumes.configMap`](#obj-spectemplatespecvolumesconfigmap)
          * [`fn withDefaultMode(defaultMode)`](#fn-spectemplatespecvolumesconfigmapwithdefaultmode)
          * [`fn withItems(items)`](#fn-spectemplatespecvolumesconfigmapwithitems)
          * [`fn withItemsMixin(items)`](#fn-spectemplatespecvolumesconfigmapwithitemsmixin)
          * [`fn withName(name)`](#fn-spectemplatespecvolumesconfigmapwithname)
          * [`fn withOptional(optional)`](#fn-spectemplatespecvolumesconfigmapwithoptional)
          * [`obj spec.template.spec.volumes.configMap.items`](#obj-spectemplatespecvolumesconfigmapitems)
            * [`fn withKey(key)`](#fn-spectemplatespecvolumesconfigmapitemswithkey)
            * [`fn withMode(mode)`](#fn-spectemplatespecvolumesconfigmapitemswithmode)
            * [`fn withPath(path)`](#fn-spectemplatespecvolumesconfigmapitemswithpath)
        * [`obj spec.template.spec.volumes.projected`](#obj-spectemplatespecvolumesprojected)
          * [`fn withDefaultMode(defaultMode)`](#fn-spectemplatespecvolumesprojectedwithdefaultmode)
          * [`fn withSources(sources)`](#fn-spectemplatespecvolumesprojectedwithsources)
          * [`fn withSourcesMixin(sources)`](#fn-spectemplatespecvolumesprojectedwithsourcesmixin)
          * [`obj spec.template.spec.volumes.projected.sources`](#obj-spectemplatespecvolumesprojectedsources)
            * [`obj spec.template.spec.volumes.projected.sources.configMap`](#obj-spectemplatespecvolumesprojectedsourcesconfigmap)
              * [`fn withItems(items)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapwithitems)
              * [`fn withItemsMixin(items)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapwithitemsmixin)
              * [`fn withName(name)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapwithname)
              * [`fn withOptional(optional)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapwithoptional)
              * [`obj spec.template.spec.volumes.projected.sources.configMap.items`](#obj-spectemplatespecvolumesprojectedsourcesconfigmapitems)
                * [`fn withKey(key)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapitemswithkey)
                * [`fn withMode(mode)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapitemswithmode)
                * [`fn withPath(path)`](#fn-spectemplatespecvolumesprojectedsourcesconfigmapitemswithpath)
            * [`obj spec.template.spec.volumes.projected.sources.downwardAPI`](#obj-spectemplatespecvolumesprojectedsourcesdownwardapi)
              * [`fn withItems(items)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiwithitems)
              * [`fn withItemsMixin(items)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiwithitemsmixin)
              * [`obj spec.template.spec.volumes.projected.sources.downwardAPI.items`](#obj-spectemplatespecvolumesprojectedsourcesdownwardapiitems)
                * [`fn withMode(mode)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemswithmode)
                * [`fn withPath(path)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemswithpath)
                * [`obj spec.template.spec.volumes.projected.sources.downwardAPI.items.fieldRef`](#obj-spectemplatespecvolumesprojectedsourcesdownwardapiitemsfieldref)
                  * [`fn withApiVersion(apiVersion)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemsfieldrefwithapiversion)
                  * [`fn withFieldPath(fieldPath)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemsfieldrefwithfieldpath)
                * [`obj spec.template.spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef`](#obj-spectemplatespecvolumesprojectedsourcesdownwardapiitemsresourcefieldref)
                  * [`fn withContainerName(containerName)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemsresourcefieldrefwithcontainername)
                  * [`fn withDivisor(divisor)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemsresourcefieldrefwithdivisor)
                  * [`fn withResource(resource)`](#fn-spectemplatespecvolumesprojectedsourcesdownwardapiitemsresourcefieldrefwithresource)
            * [`obj spec.template.spec.volumes.projected.sources.secret`](#obj-spectemplatespecvolumesprojectedsourcessecret)
              * [`fn withItems(items)`](#fn-spectemplatespecvolumesprojectedsourcessecretwithitems)
              * [`fn withItemsMixin(items)`](#fn-spectemplatespecvolumesprojectedsourcessecretwithitemsmixin)
              * [`fn withName(name)`](#fn-spectemplatespecvolumesprojectedsourcessecretwithname)
              * [`fn withOptional(optional)`](#fn-spectemplatespecvolumesprojectedsourcessecretwithoptional)
              * [`obj spec.template.spec.volumes.projected.sources.secret.items`](#obj-spectemplatespecvolumesprojectedsourcessecretitems)
                * [`fn withKey(key)`](#fn-spectemplatespecvolumesprojectedsourcessecretitemswithkey)
                * [`fn withMode(mode)`](#fn-spectemplatespecvolumesprojectedsourcessecretitemswithmode)
                * [`fn withPath(path)`](#fn-spectemplatespecvolumesprojectedsourcessecretitemswithpath)
            * [`obj spec.template.spec.volumes.projected.sources.serviceAccountToken`](#obj-spectemplatespecvolumesprojectedsourcesserviceaccounttoken)
              * [`fn withAudience(audience)`](#fn-spectemplatespecvolumesprojectedsourcesserviceaccounttokenwithaudience)
              * [`fn withExpirationSeconds(expirationSeconds)`](#fn-spectemplatespecvolumesprojectedsourcesserviceaccounttokenwithexpirationseconds)
              * [`fn withPath(path)`](#fn-spectemplatespecvolumesprojectedsourcesserviceaccounttokenwithpath)
        * [`obj spec.template.spec.volumes.secret`](#obj-spectemplatespecvolumessecret)
          * [`fn withDefaultMode(defaultMode)`](#fn-spectemplatespecvolumessecretwithdefaultmode)
          * [`fn withItems(items)`](#fn-spectemplatespecvolumessecretwithitems)
          * [`fn withItemsMixin(items)`](#fn-spectemplatespecvolumessecretwithitemsmixin)
          * [`fn withOptional(optional)`](#fn-spectemplatespecvolumessecretwithoptional)
          * [`fn withSecretName(secretName)`](#fn-spectemplatespecvolumessecretwithsecretname)
          * [`obj spec.template.spec.volumes.secret.items`](#obj-spectemplatespecvolumessecretitems)
            * [`fn withKey(key)`](#fn-spectemplatespecvolumessecretitemswithkey)
            * [`fn withMode(mode)`](#fn-spectemplatespecvolumessecretitemswithmode)
            * [`fn withPath(path)`](#fn-spectemplatespecvolumessecretitemswithpath)
  * [`obj spec.traffic`](#obj-spectraffic)
    * [`fn withConfigurationName(configurationName)`](#fn-spectrafficwithconfigurationname)
    * [`fn withLatestRevision(latestRevision)`](#fn-spectrafficwithlatestrevision)
    * [`fn withPercent(percent)`](#fn-spectrafficwithpercent)
    * [`fn withRevisionName(revisionName)`](#fn-spectrafficwithrevisionname)
    * [`fn withTag(tag)`](#fn-spectrafficwithtag)
    * [`fn withUrl(url)`](#fn-spectrafficwithurl)

## Fields

### fn new

```ts
new(name)
```

new returns an instance of Service

### fn mapContainers

```ts
mapContainers(f)
```

`mapContainers` applies the function f to each container.
It works exactly as `std.map`, but on the containers of this object.

**Signature of `f`**:
```ts
f(container: Object) Object
```


### fn mapContainersWithName

```ts
mapContainersWithName(names, f)
```

`mapContainersWithName` is like `mapContainers`, but only applies to those containers in the `names` array

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

"ServiceSpec represents the configuration for the Service object. A Service's specification is the union of the specifications for a Route and Configuration.  The Service restricts what can be expressed in these fields, e.g. the Route must reference the provided Configuration; however, these limitations also enable friendlier defaulting, e.g. Route never needs a Configuration name, and may be defaulted to the appropriate \"run latest\" spec."

### fn spec.withTraffic

```ts
withTraffic(traffic)
```

"Traffic specifies how to distribute traffic over a collection of revisions and configurations."

### fn spec.withTrafficMixin

```ts
withTrafficMixin(traffic)
```

"Traffic specifies how to distribute traffic over a collection of revisions and configurations."

**Note:** This function appends passed data to existing values

## obj spec.template

"Template holds the latest specification for the Revision to be stamped out."

## obj spec.template.metadata



### fn spec.template.metadata.withAnnotations

```ts
withAnnotations(annotations)
```



### fn spec.template.metadata.withAnnotationsMixin

```ts
withAnnotationsMixin(annotations)
```



**Note:** This function appends passed data to existing values

### fn spec.template.metadata.withFinalizers

```ts
withFinalizers(finalizers)
```



### fn spec.template.metadata.withFinalizersMixin

```ts
withFinalizersMixin(finalizers)
```



**Note:** This function appends passed data to existing values

### fn spec.template.metadata.withLabels

```ts
withLabels(labels)
```



### fn spec.template.metadata.withLabelsMixin

```ts
withLabelsMixin(labels)
```



**Note:** This function appends passed data to existing values

### fn spec.template.metadata.withName

```ts
withName(name)
```



### fn spec.template.metadata.withNamespace

```ts
withNamespace(namespace)
```



## obj spec.template.spec

"RevisionSpec holds the desired state of the Revision (from the client)."

### fn spec.template.spec.withAffinity

```ts
withAffinity(affinity)
```

"This is accessible behind a feature flag - kubernetes.podspec-affinity"

### fn spec.template.spec.withAffinityMixin

```ts
withAffinityMixin(affinity)
```

"This is accessible behind a feature flag - kubernetes.podspec-affinity"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withAutomountServiceAccountToken

```ts
withAutomountServiceAccountToken(automountServiceAccountToken)
```

"AutomountServiceAccountToken indicates whether a service account token should be automatically mounted."

### fn spec.template.spec.withContainerConcurrency

```ts
withContainerConcurrency(containerConcurrency)
```

"ContainerConcurrency specifies the maximum allowed in-flight (concurrent) requests per container of the Revision.  Defaults to `0` which means concurrency to the application is not limited, and the system decides the target concurrency for the autoscaler."

### fn spec.template.spec.withContainers

```ts
withContainers(containers)
```

"List of containers belonging to the pod. Containers cannot currently be added or removed. There must be at least one container in a Pod. Cannot be updated."

### fn spec.template.spec.withContainersMixin

```ts
withContainersMixin(containers)
```

"List of containers belonging to the pod. Containers cannot currently be added or removed. There must be at least one container in a Pod. Cannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withDnsConfig

```ts
withDnsConfig(dnsConfig)
```

"This is accessible behind a feature flag - kubernetes.podspec-dnsconfig"

### fn spec.template.spec.withDnsConfigMixin

```ts
withDnsConfigMixin(dnsConfig)
```

"This is accessible behind a feature flag - kubernetes.podspec-dnsconfig"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withDnsPolicy

```ts
withDnsPolicy(dnsPolicy)
```

"This is accessible behind a feature flag - kubernetes.podspec-dnspolicy"

### fn spec.template.spec.withEnableServiceLinks

```ts
withEnableServiceLinks(enableServiceLinks)
```

"EnableServiceLinks indicates whether information about services should be injected into pod's environment variables, matching the syntax of Docker links. Optional: Knative defaults this to false."

### fn spec.template.spec.withHostAliases

```ts
withHostAliases(hostAliases)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostaliases"

### fn spec.template.spec.withHostAliasesMixin

```ts
withHostAliasesMixin(hostAliases)
```

"This is accessible behind a feature flag - kubernetes.podspec-hostaliases"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withIdleTimeoutSeconds

```ts
withIdleTimeoutSeconds(idleTimeoutSeconds)
```

"IdleTimeoutSeconds is the maximum duration in seconds a request will be allowed to stay open while not receiving any bytes from the user's application. If unspecified, a system default will be provided."

### fn spec.template.spec.withImagePullSecrets

```ts
withImagePullSecrets(imagePullSecrets)
```

"ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod"

### fn spec.template.spec.withImagePullSecretsMixin

```ts
withImagePullSecretsMixin(imagePullSecrets)
```

"ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withInitContainers

```ts
withInitContainers(initContainers)
```

"List of initialization containers belonging to the pod. Init containers are executed in order prior to containers being started. If any init container fails, the pod is considered to have failed and is handled according to its restartPolicy. The name for an init container or normal container must be unique among all containers. Init containers may not have Lifecycle actions, Readiness probes, Liveness probes, or Startup probes. The resourceRequirements of an init container are taken into account during scheduling by finding the highest request/limit for each resource type, and then using the max of of that value or the sum of the normal containers. Limits are applied to init containers in a similar fashion. Init containers cannot currently be added or removed. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/"

### fn spec.template.spec.withInitContainersMixin

```ts
withInitContainersMixin(initContainers)
```

"List of initialization containers belonging to the pod. Init containers are executed in order prior to containers being started. If any init container fails, the pod is considered to have failed and is handled according to its restartPolicy. The name for an init container or normal container must be unique among all containers. Init containers may not have Lifecycle actions, Readiness probes, Liveness probes, or Startup probes. The resourceRequirements of an init container are taken into account during scheduling by finding the highest request/limit for each resource type, and then using the max of of that value or the sum of the normal containers. Limits are applied to init containers in a similar fashion. Init containers cannot currently be added or removed. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withNodeSelector

```ts
withNodeSelector(nodeSelector)
```

"This is accessible behind a feature flag - kubernetes.podspec-nodeselector"

### fn spec.template.spec.withNodeSelectorMixin

```ts
withNodeSelectorMixin(nodeSelector)
```

"This is accessible behind a feature flag - kubernetes.podspec-nodeselector"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withPriorityClassName

```ts
withPriorityClassName(priorityClassName)
```

"This is accessible behind a feature flag - kubernetes.podspec-priorityclassname"

### fn spec.template.spec.withResponseStartTimeoutSeconds

```ts
withResponseStartTimeoutSeconds(responseStartTimeoutSeconds)
```

"ResponseStartTimeoutSeconds is the maximum duration in seconds that the request routing layer will wait for a request delivered to a container to begin sending any network traffic."

### fn spec.template.spec.withRuntimeClassName

```ts
withRuntimeClassName(runtimeClassName)
```

"This is accessible behind a feature flag - kubernetes.podspec-runtimeclassname"

### fn spec.template.spec.withSchedulerName

```ts
withSchedulerName(schedulerName)
```

"This is accessible behind a feature flag - kubernetes.podspec-schedulername"

### fn spec.template.spec.withSecurityContext

```ts
withSecurityContext(securityContext)
```

"This is accessible behind a feature flag - kubernetes.podspec-securitycontext"

### fn spec.template.spec.withSecurityContextMixin

```ts
withSecurityContextMixin(securityContext)
```

"This is accessible behind a feature flag - kubernetes.podspec-securitycontext"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withServiceAccountName

```ts
withServiceAccountName(serviceAccountName)
```

"ServiceAccountName is the name of the ServiceAccount to use to run this pod. More info: https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/"

### fn spec.template.spec.withShareProcessNamespace

```ts
withShareProcessNamespace(shareProcessNamespace)
```

"This is accessible behind a feature flag - kubernetes.podspec-shareproccessnamespace"

### fn spec.template.spec.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"TimeoutSeconds is the maximum duration in seconds that the request instance is allowed to respond to a request. If unspecified, a system default will be provided."

### fn spec.template.spec.withTolerations

```ts
withTolerations(tolerations)
```

"This is accessible behind a feature flag - kubernetes.podspec-tolerations"

### fn spec.template.spec.withTolerationsMixin

```ts
withTolerationsMixin(tolerations)
```

"This is accessible behind a feature flag - kubernetes.podspec-tolerations"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withTopologySpreadConstraints

```ts
withTopologySpreadConstraints(topologySpreadConstraints)
```

"This is accessible behind a feature flag - kubernetes.podspec-topologyspreadconstraints"

### fn spec.template.spec.withTopologySpreadConstraintsMixin

```ts
withTopologySpreadConstraintsMixin(topologySpreadConstraints)
```

"This is accessible behind a feature flag - kubernetes.podspec-topologyspreadconstraints"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.withVolumes

```ts
withVolumes(volumes)
```

"List of volumes that can be mounted by containers belonging to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes"

### fn spec.template.spec.withVolumesMixin

```ts
withVolumesMixin(volumes)
```

"List of volumes that can be mounted by containers belonging to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.containers

"List of containers belonging to the pod. Containers cannot currently be added or removed. There must be at least one container in a Pod. Cannot be updated."

### fn spec.template.spec.containers.withArgs

```ts
withArgs(args)
```

"Arguments to the entrypoint. The container image's CMD is used if this is not provided. Variable references $(VAR_NAME) are expanded using the container's environment. If a variable cannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced to a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will produce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless of whether the variable exists or not. Cannot be updated. More info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

### fn spec.template.spec.containers.withArgsMixin

```ts
withArgsMixin(args)
```

"Arguments to the entrypoint. The container image's CMD is used if this is not provided. Variable references $(VAR_NAME) are expanded using the container's environment. If a variable cannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced to a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will produce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless of whether the variable exists or not. Cannot be updated. More info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.withCommand

```ts
withCommand(command)
```

"Entrypoint array. Not executed within a shell. The container image's ENTRYPOINT is used if this is not provided. Variable references $(VAR_NAME) are expanded using the container's environment. If a variable cannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced to a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will produce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless of whether the variable exists or not. Cannot be updated. More info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

### fn spec.template.spec.containers.withCommandMixin

```ts
withCommandMixin(command)
```

"Entrypoint array. Not executed within a shell. The container image's ENTRYPOINT is used if this is not provided. Variable references $(VAR_NAME) are expanded using the container's environment. If a variable cannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced to a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will produce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless of whether the variable exists or not. Cannot be updated. More info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.withEnv

```ts
withEnv(env)
```

"List of environment variables to set in the container. Cannot be updated."

### fn spec.template.spec.containers.withEnvFrom

```ts
withEnvFrom(envFrom)
```

"List of sources to populate environment variables in the container. The keys defined within a source must be a C_IDENTIFIER. All invalid keys will be reported as an event when the container is starting. When a key exists in multiple sources, the value associated with the last source will take precedence. Values defined by an Env with a duplicate key will take precedence. Cannot be updated."

### fn spec.template.spec.containers.withEnvFromMixin

```ts
withEnvFromMixin(envFrom)
```

"List of sources to populate environment variables in the container. The keys defined within a source must be a C_IDENTIFIER. All invalid keys will be reported as an event when the container is starting. When a key exists in multiple sources, the value associated with the last source will take precedence. Values defined by an Env with a duplicate key will take precedence. Cannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.withEnvMixin

```ts
withEnvMixin(env)
```

"List of environment variables to set in the container. Cannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.withImage

```ts
withImage(image)
```

"Container image name. More info: https://kubernetes.io/docs/concepts/containers/images This field is optional to allow higher level config management to default or override container images in workload controllers like Deployments and StatefulSets."

### fn spec.template.spec.containers.withImagePullPolicy

```ts
withImagePullPolicy(imagePullPolicy)
```

"Image pull policy. One of Always, Never, IfNotPresent. Defaults to Always if :latest tag is specified, or IfNotPresent otherwise. Cannot be updated. More info: https://kubernetes.io/docs/concepts/containers/images#updating-images"

### fn spec.template.spec.containers.withName

```ts
withName(name)
```

"Name of the container specified as a DNS_LABEL. Each container in a pod must have a unique name (DNS_LABEL). Cannot be updated."

### fn spec.template.spec.containers.withPorts

```ts
withPorts(ports)
```

"List of ports to expose from the container. Not specifying a port here DOES NOT prevent that port from being exposed. Any port which is listening on the default \"0.0.0.0\" address inside a container will be accessible from the network. Modifying this array with strategic merge patch may corrupt the data. For more information See https://github.com/kubernetes/kubernetes/issues/108255. Cannot be updated."

### fn spec.template.spec.containers.withPortsMixin

```ts
withPortsMixin(ports)
```

"List of ports to expose from the container. Not specifying a port here DOES NOT prevent that port from being exposed. Any port which is listening on the default \"0.0.0.0\" address inside a container will be accessible from the network. Modifying this array with strategic merge patch may corrupt the data. For more information See https://github.com/kubernetes/kubernetes/issues/108255. Cannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.withTerminationMessagePath

```ts
withTerminationMessagePath(terminationMessagePath)
```

"Optional: Path at which the file to which the container's termination message will be written is mounted into the container's filesystem. Message written is intended to be brief final status, such as an assertion failure message. Will be truncated by the node if greater than 4096 bytes. The total message length across all containers will be limited to 12kb. Defaults to /dev/termination-log. Cannot be updated."

### fn spec.template.spec.containers.withTerminationMessagePolicy

```ts
withTerminationMessagePolicy(terminationMessagePolicy)
```

"Indicate how the termination message should be populated. File will use the contents of terminationMessagePath to populate the container status message on both success and failure. FallbackToLogsOnError will use the last chunk of container log output if the termination message file is empty and the container exited with an error. The log output is limited to 2048 bytes or 80 lines, whichever is smaller. Defaults to File. Cannot be updated."

### fn spec.template.spec.containers.withVolumeMounts

```ts
withVolumeMounts(volumeMounts)
```

"Pod volumes to mount into the container's filesystem. Cannot be updated."

### fn spec.template.spec.containers.withVolumeMountsMixin

```ts
withVolumeMountsMixin(volumeMounts)
```

"Pod volumes to mount into the container's filesystem. Cannot be updated."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.withWorkingDir

```ts
withWorkingDir(workingDir)
```

"Container's working directory. If not specified, the container runtime's default will be used, which might be configured in the container image. Cannot be updated."

## obj spec.template.spec.containers.env

"List of environment variables to set in the container. Cannot be updated."

### fn spec.template.spec.containers.env.withName

```ts
withName(name)
```

"Name of the environment variable. Must be a C_IDENTIFIER."

### fn spec.template.spec.containers.env.withValue

```ts
withValue(value)
```

"Variable references $(VAR_NAME) are expanded using the previously defined environment variables in the container and any service environment variables. If a variable cannot be resolved, the reference in the input string will be unchanged. Double $$ are reduced to a single $, which allows for escaping the $(VAR_NAME) syntax: i.e. \"$$(VAR_NAME)\" will produce the string literal \"$(VAR_NAME)\". Escaped references will never be expanded, regardless of whether the variable exists or not. Defaults to \"\"."

## obj spec.template.spec.containers.env.valueFrom

"Source for the environment variable's value. Cannot be used if value is not empty."

### fn spec.template.spec.containers.env.valueFrom.withFieldRef

```ts
withFieldRef(fieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

### fn spec.template.spec.containers.env.valueFrom.withFieldRefMixin

```ts
withFieldRefMixin(fieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.env.valueFrom.withResourceFieldRef

```ts
withResourceFieldRef(resourceFieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

### fn spec.template.spec.containers.env.valueFrom.withResourceFieldRefMixin

```ts
withResourceFieldRefMixin(resourceFieldRef)
```

"This is accessible behind a feature flag - kubernetes.podspec-fieldref"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.containers.env.valueFrom.configMapKeyRef

"Selects a key of a ConfigMap."

### fn spec.template.spec.containers.env.valueFrom.configMapKeyRef.withKey

```ts
withKey(key)
```

"The key to select."

### fn spec.template.spec.containers.env.valueFrom.configMapKeyRef.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.containers.env.valueFrom.configMapKeyRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the ConfigMap or its key must be defined"

## obj spec.template.spec.containers.env.valueFrom.secretKeyRef

"Selects a key of a secret in the pod's namespace"

### fn spec.template.spec.containers.env.valueFrom.secretKeyRef.withKey

```ts
withKey(key)
```

"The key of the secret to select from.  Must be a valid secret key."

### fn spec.template.spec.containers.env.valueFrom.secretKeyRef.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.containers.env.valueFrom.secretKeyRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the Secret or its key must be defined"

## obj spec.template.spec.containers.envFrom

"List of sources to populate environment variables in the container. The keys defined within a source must be a C_IDENTIFIER. All invalid keys will be reported as an event when the container is starting. When a key exists in multiple sources, the value associated with the last source will take precedence. Values defined by an Env with a duplicate key will take precedence. Cannot be updated."

### fn spec.template.spec.containers.envFrom.withPrefix

```ts
withPrefix(prefix)
```

"An optional identifier to prepend to each key in the ConfigMap. Must be a C_IDENTIFIER."

## obj spec.template.spec.containers.envFrom.configMapRef

"The ConfigMap to select from"

### fn spec.template.spec.containers.envFrom.configMapRef.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.containers.envFrom.configMapRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the ConfigMap must be defined"

## obj spec.template.spec.containers.envFrom.secretRef

"The Secret to select from"

### fn spec.template.spec.containers.envFrom.secretRef.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.containers.envFrom.secretRef.withOptional

```ts
withOptional(optional)
```

"Specify whether the Secret must be defined"

## obj spec.template.spec.containers.livenessProbe

"Periodic probe of container liveness. Container will be restarted if the probe fails. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.template.spec.containers.livenessProbe.withFailureThreshold

```ts
withFailureThreshold(failureThreshold)
```

"Minimum consecutive failures for the probe to be considered failed after having succeeded. Defaults to 3. Minimum value is 1."

### fn spec.template.spec.containers.livenessProbe.withInitialDelaySeconds

```ts
withInitialDelaySeconds(initialDelaySeconds)
```

"Number of seconds after the container has started before liveness probes are initiated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.template.spec.containers.livenessProbe.withPeriodSeconds

```ts
withPeriodSeconds(periodSeconds)
```

"How often (in seconds) to perform the probe."

### fn spec.template.spec.containers.livenessProbe.withSuccessThreshold

```ts
withSuccessThreshold(successThreshold)
```

"Minimum consecutive successes for the probe to be considered successful after having failed. Defaults to 1. Must be 1 for liveness and startup. Minimum value is 1."

### fn spec.template.spec.containers.livenessProbe.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"Number of seconds after which the probe times out. Defaults to 1 second. Minimum value is 1. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

## obj spec.template.spec.containers.livenessProbe.exec

"Exec specifies the action to take."

### fn spec.template.spec.containers.livenessProbe.exec.withCommand

```ts
withCommand(command)
```

"Command is the command line to execute inside the container, the working directory for the command  is root ('/') in the container's filesystem. The command is simply exec'd, it is not run inside a shell, so traditional shell instructions ('|', etc) won't work. To use a shell, you need to explicitly call out to that shell. Exit status of 0 is treated as live/healthy and non-zero is unhealthy."

### fn spec.template.spec.containers.livenessProbe.exec.withCommandMixin

```ts
withCommandMixin(command)
```

"Command is the command line to execute inside the container, the working directory for the command  is root ('/') in the container's filesystem. The command is simply exec'd, it is not run inside a shell, so traditional shell instructions ('|', etc) won't work. To use a shell, you need to explicitly call out to that shell. Exit status of 0 is treated as live/healthy and non-zero is unhealthy."

**Note:** This function appends passed data to existing values

## obj spec.template.spec.containers.livenessProbe.grpc

"GRPC specifies an action involving a GRPC port."

### fn spec.template.spec.containers.livenessProbe.grpc.withPort

```ts
withPort(port)
```

"Port number of the gRPC service. Number must be in the range 1 to 65535."

### fn spec.template.spec.containers.livenessProbe.grpc.withService

```ts
withService(service)
```

"Service is the name of the service to place in the gRPC HealthCheckRequest (see https://github.com/grpc/grpc/blob/master/doc/health-checking.md). \n If this is not specified, the default behavior is defined by gRPC."

## obj spec.template.spec.containers.livenessProbe.httpGet

"HTTPGet specifies the http request to perform."

### fn spec.template.spec.containers.livenessProbe.httpGet.withHost

```ts
withHost(host)
```

"Host name to connect to, defaults to the pod IP. You probably want to set \"Host\" in httpHeaders instead."

### fn spec.template.spec.containers.livenessProbe.httpGet.withHttpHeaders

```ts
withHttpHeaders(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.template.spec.containers.livenessProbe.httpGet.withHttpHeadersMixin

```ts
withHttpHeadersMixin(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.livenessProbe.httpGet.withPath

```ts
withPath(path)
```

"Path to access on the HTTP server."

### fn spec.template.spec.containers.livenessProbe.httpGet.withPort

```ts
withPort(port)
```

"Name or number of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME."

### fn spec.template.spec.containers.livenessProbe.httpGet.withScheme

```ts
withScheme(scheme)
```

"Scheme to use for connecting to the host. Defaults to HTTP."

## obj spec.template.spec.containers.livenessProbe.httpGet.httpHeaders

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.template.spec.containers.livenessProbe.httpGet.httpHeaders.withName

```ts
withName(name)
```

"The header field name. This will be canonicalized upon output, so case-variant names will be understood as the same header."

### fn spec.template.spec.containers.livenessProbe.httpGet.httpHeaders.withValue

```ts
withValue(value)
```

"The header field value"

## obj spec.template.spec.containers.livenessProbe.tcpSocket

"TCPSocket specifies an action involving a TCP port."

### fn spec.template.spec.containers.livenessProbe.tcpSocket.withHost

```ts
withHost(host)
```

"Optional: Host name to connect to, defaults to the pod IP."

### fn spec.template.spec.containers.livenessProbe.tcpSocket.withPort

```ts
withPort(port)
```

"Number or name of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME."

## obj spec.template.spec.containers.ports

"List of ports to expose from the container. Not specifying a port here DOES NOT prevent that port from being exposed. Any port which is listening on the default \"0.0.0.0\" address inside a container will be accessible from the network. Modifying this array with strategic merge patch may corrupt the data. For more information See https://github.com/kubernetes/kubernetes/issues/108255. Cannot be updated."

### fn spec.template.spec.containers.ports.withContainerPort

```ts
withContainerPort(containerPort)
```

"Number of port to expose on the pod's IP address. This must be a valid port number, 0 < x < 65536."

### fn spec.template.spec.containers.ports.withName

```ts
withName(name)
```

"If specified, this must be an IANA_SVC_NAME and unique within the pod. Each named port in a pod must have a unique name. Name for the port that can be referred to by services."

### fn spec.template.spec.containers.ports.withProtocol

```ts
withProtocol(protocol)
```

"Protocol for port. Must be UDP, TCP, or SCTP. Defaults to \"TCP\"."

## obj spec.template.spec.containers.readinessProbe

"Periodic probe of container service readiness. Container will be removed from service endpoints if the probe fails. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.template.spec.containers.readinessProbe.withFailureThreshold

```ts
withFailureThreshold(failureThreshold)
```

"Minimum consecutive failures for the probe to be considered failed after having succeeded. Defaults to 3. Minimum value is 1."

### fn spec.template.spec.containers.readinessProbe.withInitialDelaySeconds

```ts
withInitialDelaySeconds(initialDelaySeconds)
```

"Number of seconds after the container has started before liveness probes are initiated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

### fn spec.template.spec.containers.readinessProbe.withPeriodSeconds

```ts
withPeriodSeconds(periodSeconds)
```

"How often (in seconds) to perform the probe."

### fn spec.template.spec.containers.readinessProbe.withSuccessThreshold

```ts
withSuccessThreshold(successThreshold)
```

"Minimum consecutive successes for the probe to be considered successful after having failed. Defaults to 1. Must be 1 for liveness and startup. Minimum value is 1."

### fn spec.template.spec.containers.readinessProbe.withTimeoutSeconds

```ts
withTimeoutSeconds(timeoutSeconds)
```

"Number of seconds after which the probe times out. Defaults to 1 second. Minimum value is 1. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes"

## obj spec.template.spec.containers.readinessProbe.exec

"Exec specifies the action to take."

### fn spec.template.spec.containers.readinessProbe.exec.withCommand

```ts
withCommand(command)
```

"Command is the command line to execute inside the container, the working directory for the command  is root ('/') in the container's filesystem. The command is simply exec'd, it is not run inside a shell, so traditional shell instructions ('|', etc) won't work. To use a shell, you need to explicitly call out to that shell. Exit status of 0 is treated as live/healthy and non-zero is unhealthy."

### fn spec.template.spec.containers.readinessProbe.exec.withCommandMixin

```ts
withCommandMixin(command)
```

"Command is the command line to execute inside the container, the working directory for the command  is root ('/') in the container's filesystem. The command is simply exec'd, it is not run inside a shell, so traditional shell instructions ('|', etc) won't work. To use a shell, you need to explicitly call out to that shell. Exit status of 0 is treated as live/healthy and non-zero is unhealthy."

**Note:** This function appends passed data to existing values

## obj spec.template.spec.containers.readinessProbe.grpc

"GRPC specifies an action involving a GRPC port."

### fn spec.template.spec.containers.readinessProbe.grpc.withPort

```ts
withPort(port)
```

"Port number of the gRPC service. Number must be in the range 1 to 65535."

### fn spec.template.spec.containers.readinessProbe.grpc.withService

```ts
withService(service)
```

"Service is the name of the service to place in the gRPC HealthCheckRequest (see https://github.com/grpc/grpc/blob/master/doc/health-checking.md). \n If this is not specified, the default behavior is defined by gRPC."

## obj spec.template.spec.containers.readinessProbe.httpGet

"HTTPGet specifies the http request to perform."

### fn spec.template.spec.containers.readinessProbe.httpGet.withHost

```ts
withHost(host)
```

"Host name to connect to, defaults to the pod IP. You probably want to set \"Host\" in httpHeaders instead."

### fn spec.template.spec.containers.readinessProbe.httpGet.withHttpHeaders

```ts
withHttpHeaders(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.template.spec.containers.readinessProbe.httpGet.withHttpHeadersMixin

```ts
withHttpHeadersMixin(httpHeaders)
```

"Custom headers to set in the request. HTTP allows repeated headers."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.readinessProbe.httpGet.withPath

```ts
withPath(path)
```

"Path to access on the HTTP server."

### fn spec.template.spec.containers.readinessProbe.httpGet.withPort

```ts
withPort(port)
```

"Name or number of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME."

### fn spec.template.spec.containers.readinessProbe.httpGet.withScheme

```ts
withScheme(scheme)
```

"Scheme to use for connecting to the host. Defaults to HTTP."

## obj spec.template.spec.containers.readinessProbe.httpGet.httpHeaders

"Custom headers to set in the request. HTTP allows repeated headers."

### fn spec.template.spec.containers.readinessProbe.httpGet.httpHeaders.withName

```ts
withName(name)
```

"The header field name. This will be canonicalized upon output, so case-variant names will be understood as the same header."

### fn spec.template.spec.containers.readinessProbe.httpGet.httpHeaders.withValue

```ts
withValue(value)
```

"The header field value"

## obj spec.template.spec.containers.readinessProbe.tcpSocket

"TCPSocket specifies an action involving a TCP port."

### fn spec.template.spec.containers.readinessProbe.tcpSocket.withHost

```ts
withHost(host)
```

"Optional: Host name to connect to, defaults to the pod IP."

### fn spec.template.spec.containers.readinessProbe.tcpSocket.withPort

```ts
withPort(port)
```

"Number or name of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME."

## obj spec.template.spec.containers.resources

"Compute Resources required by this container. Cannot be updated. More info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

### fn spec.template.spec.containers.resources.withClaims

```ts
withClaims(claims)
```

"Claims lists the names of resources, defined in spec.resourceClaims, that are used by this container. \n This is an alpha field and requires enabling the DynamicResourceAllocation feature gate. \n This field is immutable. It can only be set for containers."

### fn spec.template.spec.containers.resources.withClaimsMixin

```ts
withClaimsMixin(claims)
```

"Claims lists the names of resources, defined in spec.resourceClaims, that are used by this container. \n This is an alpha field and requires enabling the DynamicResourceAllocation feature gate. \n This field is immutable. It can only be set for containers."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.resources.withLimits

```ts
withLimits(limits)
```

"Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

### fn spec.template.spec.containers.resources.withLimitsMixin

```ts
withLimitsMixin(limits)
```

"Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.resources.withRequests

```ts
withRequests(requests)
```

"Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. Requests cannot exceed Limits. More info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

### fn spec.template.spec.containers.resources.withRequestsMixin

```ts
withRequestsMixin(requests)
```

"Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. Requests cannot exceed Limits. More info: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.containers.resources.claims

"Claims lists the names of resources, defined in spec.resourceClaims, that are used by this container. \n This is an alpha field and requires enabling the DynamicResourceAllocation feature gate. \n This field is immutable. It can only be set for containers."

### fn spec.template.spec.containers.resources.claims.withName

```ts
withName(name)
```

"Name must match the name of one entry in pod.spec.resourceClaims of the Pod where this field is used. It makes that resource available inside a container."

## obj spec.template.spec.containers.securityContext

"SecurityContext defines the security options the container should be run with. If set, the fields of SecurityContext override the equivalent fields of PodSecurityContext. More info: https://kubernetes.io/docs/tasks/configure-pod-container/security-context/"

### fn spec.template.spec.containers.securityContext.withAllowPrivilegeEscalation

```ts
withAllowPrivilegeEscalation(allowPrivilegeEscalation)
```

"AllowPrivilegeEscalation controls whether a process can gain more privileges than its parent process. This bool directly controls if the no_new_privs flag will be set on the container process. AllowPrivilegeEscalation is true always when the container is: 1) run as Privileged 2) has CAP_SYS_ADMIN Note that this field cannot be set when spec.os.name is windows."

### fn spec.template.spec.containers.securityContext.withReadOnlyRootFilesystem

```ts
withReadOnlyRootFilesystem(readOnlyRootFilesystem)
```

"Whether this container has a read-only root filesystem. Default is false. Note that this field cannot be set when spec.os.name is windows."

### fn spec.template.spec.containers.securityContext.withRunAsGroup

```ts
withRunAsGroup(runAsGroup)
```

"The GID to run the entrypoint of the container process. Uses runtime default if unset. May also be set in PodSecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence. Note that this field cannot be set when spec.os.name is windows."

### fn spec.template.spec.containers.securityContext.withRunAsNonRoot

```ts
withRunAsNonRoot(runAsNonRoot)
```

"Indicates that the container must run as a non-root user. If true, the Kubelet will validate the image at runtime to ensure that it does not run as UID 0 (root) and fail to start the container if it does. If unset or false, no such validation will be performed. May also be set in PodSecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence."

### fn spec.template.spec.containers.securityContext.withRunAsUser

```ts
withRunAsUser(runAsUser)
```

"The UID to run the entrypoint of the container process. Defaults to user specified in image metadata if unspecified. May also be set in PodSecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence. Note that this field cannot be set when spec.os.name is windows."

## obj spec.template.spec.containers.securityContext.capabilities

"The capabilities to add/drop when running containers. Defaults to the default set of capabilities granted by the container runtime. Note that this field cannot be set when spec.os.name is windows."

### fn spec.template.spec.containers.securityContext.capabilities.withAdd

```ts
withAdd(add)
```

"This is accessible behind a feature flag - kubernetes.containerspec-addcapabilities"

### fn spec.template.spec.containers.securityContext.capabilities.withAddMixin

```ts
withAddMixin(add)
```

"This is accessible behind a feature flag - kubernetes.containerspec-addcapabilities"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.containers.securityContext.capabilities.withDrop

```ts
withDrop(drop)
```

"Removed capabilities"

### fn spec.template.spec.containers.securityContext.capabilities.withDropMixin

```ts
withDropMixin(drop)
```

"Removed capabilities"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.containers.securityContext.seccompProfile

"The seccomp options to use by this container. If seccomp options are provided at both the pod & container level, the container options override the pod options. Note that this field cannot be set when spec.os.name is windows."

### fn spec.template.spec.containers.securityContext.seccompProfile.withLocalhostProfile

```ts
withLocalhostProfile(localhostProfile)
```

"localhostProfile indicates a profile defined in a file on the node should be used. The profile must be preconfigured on the node to work. Must be a descending path, relative to the kubelet's configured seccomp profile location. Must only be set if type is \"Localhost\"."

### fn spec.template.spec.containers.securityContext.seccompProfile.withType

```ts
withType(type)
```

"type indicates which kind of seccomp profile will be applied. Valid options are: \n Localhost - a profile defined in a file on the node should be used. RuntimeDefault - the container runtime default profile should be used. Unconfined - no profile should be applied."

## obj spec.template.spec.containers.volumeMounts

"Pod volumes to mount into the container's filesystem. Cannot be updated."

### fn spec.template.spec.containers.volumeMounts.withMountPath

```ts
withMountPath(mountPath)
```

"Path within the container at which the volume should be mounted.  Must not contain ':'."

### fn spec.template.spec.containers.volumeMounts.withName

```ts
withName(name)
```

"This must match the Name of a Volume."

### fn spec.template.spec.containers.volumeMounts.withReadOnly

```ts
withReadOnly(readOnly)
```

"Mounted read-only if true, read-write otherwise (false or unspecified). Defaults to false."

### fn spec.template.spec.containers.volumeMounts.withSubPath

```ts
withSubPath(subPath)
```

"Path within the volume from which the container's volume should be mounted. Defaults to \"\" (volume's root)."

## obj spec.template.spec.imagePullSecrets

"ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod"

### fn spec.template.spec.imagePullSecrets.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

## obj spec.template.spec.volumes

"List of volumes that can be mounted by containers belonging to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes"

### fn spec.template.spec.volumes.withEmptyDir

```ts
withEmptyDir(emptyDir)
```

"This is accessible behind a feature flag - kubernetes.podspec-emptydir"

### fn spec.template.spec.volumes.withEmptyDirMixin

```ts
withEmptyDirMixin(emptyDir)
```

"This is accessible behind a feature flag - kubernetes.podspec-emptydir"

**Note:** This function appends passed data to existing values

### fn spec.template.spec.volumes.withName

```ts
withName(name)
```

"name of the volume. Must be a DNS_LABEL and unique within the pod. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names"

### fn spec.template.spec.volumes.withPersistentVolumeClaim

```ts
withPersistentVolumeClaim(persistentVolumeClaim)
```

"This is accessible behind a feature flag - kubernetes.podspec-persistent-volume-claim"

### fn spec.template.spec.volumes.withPersistentVolumeClaimMixin

```ts
withPersistentVolumeClaimMixin(persistentVolumeClaim)
```

"This is accessible behind a feature flag - kubernetes.podspec-persistent-volume-claim"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.volumes.configMap

"configMap represents a configMap that should populate this volume"

### fn spec.template.spec.volumes.configMap.withDefaultMode

```ts
withDefaultMode(defaultMode)
```

"defaultMode is optional: mode bits used to set permissions on created files by default. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. Defaults to 0644. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.configMap.withItems

```ts
withItems(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.configMap.withItemsMixin

```ts
withItemsMixin(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.volumes.configMap.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.volumes.configMap.withOptional

```ts
withOptional(optional)
```

"optional specify whether the ConfigMap or its keys must be defined"

## obj spec.template.spec.volumes.configMap.items

"items if unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.configMap.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.template.spec.volumes.configMap.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.configMap.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to. May not be an absolute path. May not contain the path element '..'. May not start with the string '..'."

## obj spec.template.spec.volumes.projected

"projected items for all in one resources secrets, configmaps, and downward API"

### fn spec.template.spec.volumes.projected.withDefaultMode

```ts
withDefaultMode(defaultMode)
```

"defaultMode are the mode bits used to set permissions on created files by default. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.projected.withSources

```ts
withSources(sources)
```

"sources is the list of volume projections"

### fn spec.template.spec.volumes.projected.withSourcesMixin

```ts
withSourcesMixin(sources)
```

"sources is the list of volume projections"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.volumes.projected.sources

"sources is the list of volume projections"

## obj spec.template.spec.volumes.projected.sources.configMap

"configMap information about the configMap data to project"

### fn spec.template.spec.volumes.projected.sources.configMap.withItems

```ts
withItems(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.projected.sources.configMap.withItemsMixin

```ts
withItemsMixin(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.volumes.projected.sources.configMap.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.volumes.projected.sources.configMap.withOptional

```ts
withOptional(optional)
```

"optional specify whether the ConfigMap or its keys must be defined"

## obj spec.template.spec.volumes.projected.sources.configMap.items

"items if unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.projected.sources.configMap.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.template.spec.volumes.projected.sources.configMap.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.projected.sources.configMap.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to. May not be an absolute path. May not contain the path element '..'. May not start with the string '..'."

## obj spec.template.spec.volumes.projected.sources.downwardAPI

"downwardAPI information about the downwardAPI data to project"

### fn spec.template.spec.volumes.projected.sources.downwardAPI.withItems

```ts
withItems(items)
```

"Items is a list of DownwardAPIVolume file"

### fn spec.template.spec.volumes.projected.sources.downwardAPI.withItemsMixin

```ts
withItemsMixin(items)
```

"Items is a list of DownwardAPIVolume file"

**Note:** This function appends passed data to existing values

## obj spec.template.spec.volumes.projected.sources.downwardAPI.items

"Items is a list of DownwardAPIVolume file"

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.withMode

```ts
withMode(mode)
```

"Optional: mode bits used to set permissions on this file, must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.withPath

```ts
withPath(path)
```

"Required: Path is  the relative path name of the file to be created. Must not be absolute or contain the '..' path. Must be utf-8 encoded. The first item of the relative path must not start with '..'"

## obj spec.template.spec.volumes.projected.sources.downwardAPI.items.fieldRef

"Required: Selects a field of the pod: only annotations, labels, name and namespace are supported."

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.fieldRef.withApiVersion

```ts
withApiVersion(apiVersion)
```

"Version of the schema the FieldPath is written in terms of, defaults to \"v1\"."

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.fieldRef.withFieldPath

```ts
withFieldPath(fieldPath)
```

"Path of the field to select in the specified API version."

## obj spec.template.spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef

"Selects a resource of the container: only resources limits and requests (limits.cpu, limits.memory, requests.cpu and requests.memory) are currently supported."

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef.withContainerName

```ts
withContainerName(containerName)
```

"Container name: required for volumes, optional for env vars"

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef.withDivisor

```ts
withDivisor(divisor)
```

"Specifies the output format of the exposed resources, defaults to \"1\

### fn spec.template.spec.volumes.projected.sources.downwardAPI.items.resourceFieldRef.withResource

```ts
withResource(resource)
```

"Required: resource to select"

## obj spec.template.spec.volumes.projected.sources.secret

"secret information about the secret data to project"

### fn spec.template.spec.volumes.projected.sources.secret.withItems

```ts
withItems(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.projected.sources.secret.withItemsMixin

```ts
withItemsMixin(items)
```

"items if unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.volumes.projected.sources.secret.withName

```ts
withName(name)
```

"Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?"

### fn spec.template.spec.volumes.projected.sources.secret.withOptional

```ts
withOptional(optional)
```

"optional field specify whether the Secret or its key must be defined"

## obj spec.template.spec.volumes.projected.sources.secret.items

"items if unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.projected.sources.secret.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.template.spec.volumes.projected.sources.secret.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.projected.sources.secret.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to. May not be an absolute path. May not contain the path element '..'. May not start with the string '..'."

## obj spec.template.spec.volumes.projected.sources.serviceAccountToken

"serviceAccountToken is information about the serviceAccountToken data to project"

### fn spec.template.spec.volumes.projected.sources.serviceAccountToken.withAudience

```ts
withAudience(audience)
```

"audience is the intended audience of the token. A recipient of a token must identify itself with an identifier specified in the audience of the token, and otherwise should reject the token. The audience defaults to the identifier of the apiserver."

### fn spec.template.spec.volumes.projected.sources.serviceAccountToken.withExpirationSeconds

```ts
withExpirationSeconds(expirationSeconds)
```

"expirationSeconds is the requested duration of validity of the service account token. As the token approaches expiration, the kubelet volume plugin will proactively rotate the service account token. The kubelet will start trying to rotate the token if the token is older than 80 percent of its time to live or if the token is older than 24 hours.Defaults to 1 hour and must be at least 10 minutes."

### fn spec.template.spec.volumes.projected.sources.serviceAccountToken.withPath

```ts
withPath(path)
```

"path is the path relative to the mount point of the file to project the token into."

## obj spec.template.spec.volumes.secret

"secret represents a secret that should populate this volume. More info: https://kubernetes.io/docs/concepts/storage/volumes#secret"

### fn spec.template.spec.volumes.secret.withDefaultMode

```ts
withDefaultMode(defaultMode)
```

"defaultMode is Optional: mode bits used to set permissions on created files by default. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. Defaults to 0644. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.secret.withItems

```ts
withItems(items)
```

"items If unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.secret.withItemsMixin

```ts
withItemsMixin(items)
```

"items If unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

**Note:** This function appends passed data to existing values

### fn spec.template.spec.volumes.secret.withOptional

```ts
withOptional(optional)
```

"optional field specify whether the Secret or its keys must be defined"

### fn spec.template.spec.volumes.secret.withSecretName

```ts
withSecretName(secretName)
```

"secretName is the name of the secret in the pod's namespace to use. More info: https://kubernetes.io/docs/concepts/storage/volumes#secret"

## obj spec.template.spec.volumes.secret.items

"items If unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'."

### fn spec.template.spec.volumes.secret.items.withKey

```ts
withKey(key)
```

"key is the key to project."

### fn spec.template.spec.volumes.secret.items.withMode

```ts
withMode(mode)
```

"mode is Optional: mode bits used to set permissions on this file. Must be an octal value between 0000 and 0777 or a decimal value between 0 and 511. YAML accepts both octal and decimal values, JSON requires decimal values for mode bits. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set."

### fn spec.template.spec.volumes.secret.items.withPath

```ts
withPath(path)
```

"path is the relative path of the file to map the key to. May not be an absolute path. May not contain the path element '..'. May not start with the string '..'."

## obj spec.traffic

"Traffic specifies how to distribute traffic over a collection of revisions and configurations."

### fn spec.traffic.withConfigurationName

```ts
withConfigurationName(configurationName)
```

"ConfigurationName of a configuration to whose latest revision we will send this portion of traffic. When the \"status.latestReadyRevisionName\" of the referenced configuration changes, we will automatically migrate traffic from the prior \"latest ready\" revision to the new one.  This field is never set in Route's status, only its spec.  This is mutually exclusive with RevisionName."

### fn spec.traffic.withLatestRevision

```ts
withLatestRevision(latestRevision)
```

"LatestRevision may be optionally provided to indicate that the latest ready Revision of the Configuration should be used for this traffic target.  When provided LatestRevision must be true if RevisionName is empty; it must be false when RevisionName is non-empty."

### fn spec.traffic.withPercent

```ts
withPercent(percent)
```

"Percent indicates that percentage based routing should be used and the value indicates the percent of traffic that is be routed to this Revision or Configuration. `0` (zero) mean no traffic, `100` means all traffic. When percentage based routing is being used the follow rules apply: - the sum of all percent values must equal 100 - when not specified, the implied value for `percent` is zero for that particular Revision or Configuration"

### fn spec.traffic.withRevisionName

```ts
withRevisionName(revisionName)
```

"RevisionName of a specific revision to which to send this portion of traffic.  This is mutually exclusive with ConfigurationName."

### fn spec.traffic.withTag

```ts
withTag(tag)
```

"Tag is optionally used to expose a dedicated url for referencing this target exclusively."

### fn spec.traffic.withUrl

```ts
withUrl(url)
```

"URL displays the URL for accessing named traffic targets. URL is displayed in status, and is disallowed on spec. URL must contain a scheme (e.g. http://) and a hostname, but may not contain anything else (e.g. basic auth, url path, etc.)"