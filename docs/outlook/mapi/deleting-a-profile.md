---
title: Excluir um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573240"
---
# <a name="deleting-a-profile"></a>Excluir um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para excluir um perfil**
  
- Chame [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca o perfil para exclusão, se ele está sendo usado atualmente, aguardar até que ele não está mais ativo para removê-lo. O perfil não desapareça realmente até que cada cliente com uma sessão ativa desconectado. 
  
 **DeleteProfile** chama a função do ponto de entrada de cada serviço de mensagem no perfil com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE. As chamadas para as funções de ponto de entrada ocorrerem antes que os serviços são removidos fisicamente do perfil. 
  

