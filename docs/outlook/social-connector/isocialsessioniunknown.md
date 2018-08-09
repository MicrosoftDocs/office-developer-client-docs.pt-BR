---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Representa uma conexão a um site de rede social.
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770873"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Representa uma conexão a um site de rede social.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession** . 
  
|**Name**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Método  <br/> |Obtém um string que representa uma ou mais pessoas que coincidem com o parâmetro _userID_ .  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Método  <br/> |Adiciona a pessoa identificada pelo parâmetro _emailAddress_ como um amigo para o usuário de logon na rede social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Método  <br/> |Este método foi preterido no Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Método  <br/> |Obtém uma interface [ISocialProfile](isocialprofileisocialperson.md) que representa o usuário conectado.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Método  <br/> |Obtém um string que representa uma URL que é usada para apresentar um formulário baseado em navegador para o usuário durante a autenticação da web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Método  <br/> |Obtém um string que representa um identificador exclusivo de redes sociais para uma conexão de rede social fornecido.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Método  <br/> |Obtém uma interface [ISocialPerson](isocialpersoniunknown.md) com base em que o parâmetro _userID_ .  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Propriedade  <br/> |Retorna uma string que representa a ID de usuário de redes sociais do usuário que está conectado no momento.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Propriedade  <br/> |Retorna uma string que representa o nome de usuário que é usado quando o logon.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Método  <br/> |Logs para o site de rede social usando o nome de usuário especificado e a senha.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Método  <br/> |Logs para o site de rede social usando a autenticação baseada em formulários.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Propriedade  <br/> |Define a URL do site de rede social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Método  <br/> |Remove a pessoa identificada pelo parâmetro _userID_ como um amigo na rede social.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor OSC deve implementar essa interface para se comunicar com o OSC.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

