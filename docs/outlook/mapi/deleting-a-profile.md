---
title: Exclusão de um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766384"
---
# <a name="deleting-a-profile"></a>Exclusão de um perfil

  
  
**Aplica-se a**: Outlook 
  
 **Para excluir um perfil**
  
- Chame [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca o perfil para exclusão, se ele está sendo usado atualmente, aguardar até que ele não está mais ativo para removê-lo. O perfil não desapareça realmente até que cada cliente com uma sessão ativa desconectado. 
  
 **DeleteProfile** chama a função do ponto de entrada de cada serviço de mensagem no perfil com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE. As chamadas para as funções de ponto de entrada ocorrerem antes que os serviços são removidos fisicamente do perfil. 
  

