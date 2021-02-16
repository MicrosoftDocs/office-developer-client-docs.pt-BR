---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica deixar uma cópia de uma mensagem no servidor para uma conta POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410942"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

Especifica deixar uma cópia de uma mensagem no servidor para uma conta POP.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador:  <br/> |0x1000  <br/> |
|Tipo de propriedade:  <br/> |PT_DWORD  <br/> |
|Marca de propriedade:  <br/> |0x10000003  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir lista os valores possíveis. Consulte [Constantes (API de gerenciamento de conta)](constants-account-management-api.md) para obter mais informações sobre as constantes. 
  
|**Valores possíveis**|**Descrição**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Deixa uma cópia da mensagem no servidor POP após baixar a mensagem para um dispositivo.  <br/> |
|**REMOVE_AFTER** <br/> |Remove a mensagem do servidor POP depois de baixá-la para um dispositivo.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Remove a mensagem do servidor POP somente depois que o usuário excluir a mensagem da pasta Itens Excluídos.  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |Obtém o número de dias após os quais a mensagem será removida do servidor POP.  <br/> |
|**SET_REMOVE_AFTER_DAYS**( _dias_)  <br/> |Define o número de dias após os quais a mensagem será removida do servidor POP.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)

