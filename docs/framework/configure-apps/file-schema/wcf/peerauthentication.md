---
title: '&lt;peerAuthentication&gt;'
ms.date: 03/30/2017
ms.assetid: ad545e6f-f06e-4549-ac92-09d758d5c636
ms.openlocfilehash: 4d84ffc3fbca03e43c34808e03a57b015898ee07
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33352449"
---
# <a name="ltpeerauthenticationgt"></a>&lt;peerAuthentication&gt;
指定对等节点使用的对等证书的身份验证设置。  
  
 \<system.ServiceModel>  
\<行为 >  
\<serviceBehaviors>  
\<行为 >  
\<serviceCredentials>  
\<对等 >  
\<peerAuthentication>  
  
## <a name="syntax"></a>语法  
  
```xml  
<peerAuthentication  
      customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"  
      certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"  
      revocationMode="NoCheck/Online/Offline"  
      trustedStoreLocation="CurrentUser/LocalMachine"   
/>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|`certificateValidationMode`|可选的枚举。 指定用来验证凭据的三种模式之一。 此属性的类型为 <xref:System.ServiceModel.Security.X509CertificateValidationMode>。 如果设置为 `Custom`，则还必须提供 `customCertificateValidator`。|  
|`customCertificateValidatorType`|可选的字符串。 指定用于验证自定义类型的类型和程序集。 当 `certificateValidationMode` 设置为 `Custom` 时，必须设置此属性。 此属性的类型为 <xref:System.IdentityModel.Selectors.X509CertificateValidator>。 Windows Communication Foundation (WCF) 提供一个默认对等证书验证程序，用于验证针对受信任的人存储的对等证书。 它还验证证书是否与有效的根相联系。 您可以实现自定义验证程序以指定不同的行为，并使用该属性指向自定义验证程序。|  
|`revocationMode`|可选的枚举。 指定证书吊销模式。 此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>。 系统通过在吊销证书列表中进行查找来验证对等证书尚未吊销。 可以联机执行该检查，也可以根据缓存的吊销列表执行该检查。 将此属性设置为 NoCheck 可禁用吊销检查。|  
|`trustedStoreLocation`|可选的枚举。 指定对等证书验证 WCF 安全系统的受信任存储区位置。 此属性的类型为 <xref:System.Security.Cryptography.X509Certificates.StoreLocation>。|  
  
### <a name="child-elements"></a>子元素  
 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<peer>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-servicecredentials.md)|指定对等节点的当前凭据。|  
  
## <a name="remarks"></a>备注  
 `<authentication>` 元素与 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> 类相对应。 此元素指定一个验证程序，在网格中执行邻居对等身份验证的过程中将调用该验证程序。 当新对等方尝试建立邻居连接时，它会将自己的凭据传递到响应的对等方。 将调用响应方的验证程序来验证远程方的凭据。 每当在网格中建立对等连接时，对等方将会相互进行身份验证，这意味着会同时在两方调用验证程序。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement>  
 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>  
 <xref:System.ServiceModel.Security.PeerCredential.PeerAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.PeerAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>  
 [使用证书](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [对等网络](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [对等通道消息身份验证](http://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [对等通道自定义身份验证](http://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [保护对等通道应用程序](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
