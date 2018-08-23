---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f182610f9cf4874cc18c409960e1f8b23f853d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574822"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que as soluções do Microsoft Outlook 2010 e o Microsoft Outlook 2013 descobrir se um anexo é considerado não seguros e bloqueados para exibição e indexação.
  
|||
|:-----|:-----|
|Identificador de interface:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Verifica se um anexo especificado é bloqueado pelo Outlook 2010 ou Outlook 2013 para exibição e indexação.  <br/> |
   
## <a name="remarks"></a>Comentários

Soluções do Outlook 2010 e o Outlook 2013 podem consultar a esta interface para ver se um anexo estiver bloqueado. Os anexos que serão bloqueados pelo Outlook 2010 ou Outlook 2013 variam dependendo de como o Outlook 2010 ou Outlook 2013 foi configurado e as políticas que um administrador tiver sido aplicada.
  
## <a name="see-also"></a>Confira também



[Constantes MAPI](mapi-constants.md)
  
[Verificar se um anexo foi bloqueado](how-to-verify-an-attachment-is-blocked.md)

