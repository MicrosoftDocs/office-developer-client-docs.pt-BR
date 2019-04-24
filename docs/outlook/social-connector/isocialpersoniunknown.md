---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Representa uma pessoa na rede social.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331938"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Representa uma pessoa na rede social.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialPerson** . 
  
|**Nome**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Método		  <br/> |Esse método foi preterido desde o Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Método		  <br/> |Obtém uma cadeia de caracteres que representa detalhes para a pessoa, como nome, sobrenome e URL de uma imagem de perfil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Método		  <br/> |Obtém uma cadeia de caracteres que representa uma coleção de pessoas.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Método		  <br/> |No momento, este método não tem suporte.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Método		  <br/> |Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Método		  <br/> |No momento, este método não tem suporte.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor do Outlook Social Connector (OSC) deve implementar essa interface para se comunicar com o OSC.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

