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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766883"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Permite que as soluções do Microsoft Outlook 2010 e o Microsoft Outlook 2013 descobrir se um anexo é considerado não seguros e bloqueados para exibição e indexação.
  
|||
|:-----|:-----|
|Identificador de interface:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Verifica se um anexo especificado é bloqueado pelo Outlook 2010 ou Outlook 2013 para exibição e indexação.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Soluções do Outlook 2010 e o Outlook 2013 podem consultar a esta interface para ver se um anexo estiver bloqueado. Os anexos que serão bloqueados pelo Outlook 2010 ou Outlook 2013 variam dependendo de como o Outlook 2010 ou Outlook 2013 foi configurado e as políticas que um administrador tiver sido aplicada.
  
## <a name="see-also"></a>Confira também



[Constantes MAPI](mapi-constants.md)
  
[Verifique se que um anexo estiver bloqueado](how-to-verify-an-attachment-is-blocked.md)

