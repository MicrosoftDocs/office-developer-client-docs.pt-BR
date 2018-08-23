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
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564168"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

