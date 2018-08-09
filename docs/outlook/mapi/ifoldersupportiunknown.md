---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766958"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Fornece informações sobre o suporte de uma pasta para compartilhamento.
  
|||
|:-----|:-----|
|Provided by:  <br/> |Provedor de armazenamento de mensagem  <br/> |
|Identificador de interface:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtém informações sobre o suporte de uma pasta para compartilhamento.  <br/> |
   
## <a name="remarks"></a>Comentários

Geralmente, o Microsoft Office Outlook requer um MAPI armazenar provedor implemente essa interface se o provedor quer compartilhar uma pasta. A exceção é o provedor de repositório do Exchange Server, que pode compartilhar pastas sem implementar esta interface.
  
Um cliente pode consultar um **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**. Se tiver êxito, chame **IFolderSupport::GetSupportMask** e procurar estará definido o bit **FS_SUPPORTS_SHARING** a ser definido. 
  

