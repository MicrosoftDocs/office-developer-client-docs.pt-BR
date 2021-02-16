---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429044"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador de entrada composto para um objeto, geralmente uma mensagem em um armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>Parâmetros

 _psession_
  
> [in] Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _cbStoreRecordKey_
  
> [in] Tamanho, em bytes, da chave de registro do armazenamento de mensagens que mantém a mensagem ou outro objeto. Se zero for passado no parâmetro  _cbStoreRecordKey,_ o parâmetro  _ppEID_ aponta para uma cópia do identificador de entrada do objeto. 
    
 _pStoreRecordKey_
  
> [in] Ponteiro para a tecla de registro do armazenamento de mensagens que contém a mensagem ou outro objeto. 
    
 _cbMsgEID_
  
> [in] Tamanho, em bytes, do identificador de entrada da mensagem ou de outro objeto. 
    
 _pMsgEID_
  
> [in] Ponteiro para o identificador de entrada do objeto. 
    
 _pcbEID_
  
> [out] Ponteiro para o tamanho, em bytes, do identificador retornado. 
    
 _ppEID_
  
> [out] Ponteiro para um ponteiro para o identificador de entrada retornado. Se o valor do parâmetro  _cbStoreRecordKey_ for maior que zero, o parâmetro  _ppEID_ aponta para um ponteiro para o identificador de entrada composto criado. Se  _cbStoreRecordKey_ for zero,  _ppEID_ aponta para um ponteiro para uma cópia do identificador de entrada do objeto. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se a mensagem ou outro objeto para o qual o identificador de entrada composta está sendo criado residir em um armazenamento de mensagens, o identificador será criado a partir do identificador de entrada do objeto e da chave de registro do armazenamento. Se o objeto não estiver em um repositório, ou seja, se a contagem de byte para a chave de registro do repositório passada em  _cbStoreRecordKey_ for zero, o identificador de entrada do objeto será simplesmente copiado. 
  
A **função HrComposeEID** permite que os aplicativos trabalhem com objetos em vários armazenamentos por meio do uso de identificadores de entrada compostos. Um aplicativo pode chamar [a função HrDecomposeEID](hrdecomposeeid.md) para dividir o identificador de entrada composta em seus componentes originais. 
  
## <a name="see-also"></a>Confira também



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

