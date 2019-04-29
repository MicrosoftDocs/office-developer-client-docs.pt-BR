---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436108"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Separa o identificador de entrada composta de um objeto, geralmente uma mensagem em um repositório de mensagens, no identificador de entrada desse objeto no repositório e no identificador de entrada da loja.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parâmetros

 _psession_
  
> no Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _cbEID_
  
> no Tamanho, em bytes, do identificador de entrada composta a ser separado. 
    
 _pEID_
  
> no Ponteiro para o identificador de entrada composta a ser separado. 
    
 _pcbStoreEID_
  
> bota Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagens que contém o objeto. Se o parâmetro _pEID_ apontar para um identificador de entrada não composta, o parâmetro _pcbStoreEID_ apontará para um valor igual a zero. 
    
 _ppStoreEID_
  
> bota Ponteiro para um ponteiro para o identificador de entrada retornado do repositório de mensagens que contém o objeto. Se o parâmetro _pEID_ apontar para um identificador de entrada não composta, NULL será retornado no parâmetro _ppStoreEID_ . 
    
 _pcbMsgEID_
  
> bota Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto. Se o parâmetro _pEID_ apontar para um identificador de entrada não composta, o parâmetro _pcbMsgEID_ será igual ao valor do parâmetro _cbEID_ . 
    
 _ppMsgEID_
  
> bota Ponteiro para um ponteiro para o identificador de entrada retornado do objeto. Se o parâmetro _pEID_ apontar para um identificador de entrada não composta, _ppMsgEID_ apontará para um ponteiro para uma cópia do identificador de entrada não composto. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se o identificador especificado pelo parâmetro _pEID_ for composto, ele será dividido no identificador de entrada do objeto em seu repositório de mensagens e no identificador de entrada da loja. Cadeias de caracteres de identificador de entrada não compostos são simplesmente copiadas. O identificador composto a ser separado é normalmente um criado pela função [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A memória que mantém o parâmetro _pEID_ é liberada após a conclusão com êxito da função. A implementação de chamada é responsável por liberar memória para os parâmetros de saída. 
  

