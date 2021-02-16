---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Representa uma pessoa nas redes sociais.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407008"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Representa uma pessoa nas redes sociais.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialPerson.** 
  
|**Nome**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Method  <br/> |Esse método foi preterido desde o Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que representa detalhes da pessoa, como o nome, sobrenome e uma URL para uma imagem de perfil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que representa uma coleção de pessoas.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Method  <br/> |No momento, não há suporte para esse método.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Method  <br/> |Obtém uma matriz de bytes que contém o recurso de imagem da pessoa.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Method  <br/> |No momento, não há suporte para esse método.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor do Outlook Social Connector (OSC) deve implementar essa interface para se comunicar com o OSC.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

