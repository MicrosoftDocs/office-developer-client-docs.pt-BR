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
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326982"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que as soluções do Microsoft Outlook 2010 e do Microsoft Outlook 2013 descubram se um anexo é considerado não seguro e bloqueado para visualização e indexação.
  
|||
|:-----|:-----|
|Identificador de interface:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Verifica se um anexo especificado está bloqueado pelo Outlook 2010 ou pelo Outlook 2013 para exibição e indexação.  <br/> |
   
## <a name="remarks"></a>Comentários

As soluções do Outlook 2010 e do Outlook 2013 podem consultar essa interface para ver se um anexo está bloqueado. Os anexos bloqueados pelo Outlook 2010 ou o Outlook 2013 variam de acordo com o modo como o Outlook 2010 ou o Outlook 2013 foi configurado e as políticas aplicadas por um administrador.
  
## <a name="see-also"></a>Confira também



[Constantes de MAPI](mapi-constants.md)
  
[Verificar se um anexo está bloqueado](how-to-verify-an-attachment-is-blocked.md)

