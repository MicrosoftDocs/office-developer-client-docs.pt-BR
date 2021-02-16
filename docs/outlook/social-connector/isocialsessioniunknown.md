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
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437823"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Representa uma conexão a um site de rede social.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialSession.** 
  
|**Nome**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que representa uma ou mais pessoas que corresponderem ao _parâmetro userID._  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Method  <br/> |Adiciona a pessoa identificada pelo  _parâmetro emailAddress_ como um amigo do usuário conectado na rede social.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Method  <br/> |Esse método foi preterido no Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Method  <br/> |Obtém uma interface [ISocialProfile](isocialprofileisocialperson.md) que representa o usuário conectado.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que representa uma URL usada para apresentar um formulário baseado em navegador para o usuário durante a autenticação da Web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que representa um identificador de rede social exclusivo para uma determinada conexão de rede social.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Method  <br/> |Obtém uma interface [ISocialPerson](isocialpersoniunknown.md) com base no _parâmetro userID._  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Propriedade  <br/> |Retorna uma cadeia de caracteres que representa a ID de usuário da rede social do usuário que está conectado no momento.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Propriedade  <br/> |Retorna uma cadeia de caracteres que representa o nome de usuário usado ao fazer logor.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Method  <br/> |Faz logon no site da rede social usando o nome de usuário e a senha especificados.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Method  <br/> |Faz o login no site da rede social usando a autenticação baseada em formulários.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Propriedade  <br/> |Define a URL do site da rede social.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Method  <br/> |Remove a pessoa identificada pelo  _parâmetro userID_ como um amigo na rede social.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor OSC deve implementar essa interface para se comunicar com o OSC.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

