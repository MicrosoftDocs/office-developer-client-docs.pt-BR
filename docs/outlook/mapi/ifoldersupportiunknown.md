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
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415772"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações sobre o suporte de uma pasta para compartilhamento.
  
|||
|:-----|:-----|
|Provided by:  <br/> |Provedor de armazenamento de mensagens  <br/> |
|Identificador de interface:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |Obtém informações sobre o suporte de uma pasta para compartilhamento.  <br/> |
   
## <a name="remarks"></a>Comentários

Geralmente, o Microsoft Office Outlook requer um provedor de armazenamento MAPI para implementar essa interface se o provedor quiser compartilhar uma pasta. A exceção é o provedor de armazenamento do Exchange Server, que pode compartilhar pastas sem implementar essa interface.
  
Um cliente pode consultar uma **[IMAPIFolder](imapifolderimapicontainer.md)** para **IFolderSupport**. Se isso for bem-sucedido, chame **IFolderSupport::GetSupportMask** e verifique se FS_SUPPORTS_SHARING **bit** a ser definido. 
  

