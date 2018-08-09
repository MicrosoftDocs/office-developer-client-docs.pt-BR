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
ms.openlocfilehash: d6fca18ac2d2074239bd8b435bcd40971de83670
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770842"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Representa uma pessoa na rede social.
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialPerson** . 
  
|**Name**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Método  <br/> |Este método foi preterido desde o Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Método  <br/> |Obtém um string que representa os detalhes para a pessoa, como o primeiro nome, sobrenome e uma URL para uma imagem de perfil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Método  <br/> |Obtém um string que representa uma coleção de pessoas.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Método  <br/> |Esse método não é suportado no momento.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Método  <br/> |Obtém uma matriz de bytes que contém o recurso de imagem para a pessoa.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Método  <br/> |Esse método não é suportado no momento.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor do Outlook Social Connector (OSC) deve implementar essa interface para se comunicar com o OSC.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

