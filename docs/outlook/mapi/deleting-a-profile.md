---
title: Excluindo um perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410200"
---
# <a name="deleting-a-profile"></a>Excluindo um perfil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para excluir um perfil**
  
- Chame [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** marca o perfil para exclusão se ele estiver sendo usado no momento, aguardando até que ele não está mais ativo para removê-lo. Na verdade, o perfil não desaparece até que todos os clientes com uma sessão ativa se desconectem. 
  
 **DeleteProfile** chama a função de ponto de entrada de cada serviço de mensagem no perfil com o  _parâmetro ulContext_ definido como MSG_SERVICE_DELETE. As chamadas para as funções de ponto de entrada ocorrem antes que os serviços sejam fisicamente removidos do perfil. 
  

