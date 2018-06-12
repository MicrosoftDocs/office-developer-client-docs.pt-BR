---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica a deixar uma cópia de uma mensagem no servidor para uma conta POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766062"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

Especifica a deixar uma cópia de uma mensagem no servidor para uma conta POP.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador:  <br/> |0x1000  <br/> |
|Tipo de propriedade:  <br/> |PT_DWORD  <br/> |
|Marca de propriedade:  <br/> |0x10000003  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Coment�rios

A tabela a seguir lista os valores possíveis. Consulte [constantes (API de gerenciamento de conta)](constants-account-management-api.md) para obter mais informações sobre as constantes. 
  
|**Valores possíveis**|**Descrição**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Deixar uma cópia da mensagem no servidor POP depois de baixar a mensagem a um dispositivo.  <br/> |
|**REMOVE_AFTER** <br/> |Remove a mensagem do servidor POP após fazer o download em um dispositivo.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Remove a mensagem do servidor POP somente depois que o usuário excluir a mensagem da pasta Itens excluídos.  <br/> |
|**GET_REMOVE_AFTER_DAYS** ( _ul_)  <br/> |Obtém o número de dias após o qual a mensagem será removida do servidor POP.  <br/> |
|**SET_REMOVE_AFTER_DAYS** ( _dias_)  <br/> |Define o número de dias após o qual a mensagem será removida do servidor POP.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Gerenciando mensagem downloads para contas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

