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
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564812"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador compostos de entrada para um objeto, geralmente em uma mensagem em um armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> [in] Tamanho, em bytes, da chave do registro do armazenamento de mensagens, mantendo a mensagem ou outro objeto. Se o parâmetro _cbStoreRecordKey_ é passado zero, o parâmetro _ppEID_ aponta para uma cópia do identificador de entrada do objeto. 
    
 _pStoreRecordKey_
  
> [in] Ponteiro para a chave de registro do repositório de mensagem que contém a mensagem ou outro objeto. 
    
 _cbMsgEID_
  
> [in] Tamanho, em bytes, do identificador de entrada de mensagem ou outro objeto. 
    
 _pMsgEID_
  
> [in] Ponteiro para o identificador de entrada do objeto. 
    
 _pcbEID_
  
> [out] Ponteiro para o tamanho, em bytes, do identificador retornado. 
    
 _ppEID_
  
> [out] Ponteiro para um ponteiro para o identificador de entrada retornados. Se o valor do parâmetro _cbStoreRecordKey_ for maior do que zero, o parâmetro _ppEID_ aponta para um ponteiro para o identificador de entrada compostos que é criado. Se _cbStoreRecordKey_ for zero, _ppEID_ aponta para um ponteiro para uma cópia do identificador de entrada do objeto. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se a mensagem ou outro objeto para o qual está sendo criado o identificador de entrada compostos residir em um armazenamento de mensagens, o identificador é criado do identificador de entrada do objeto e a chave do registro da loja. Se o objeto não estiver em um repositório, ou seja, se o número de bytes para a chave de registro do repositório passada em _cbStoreRecordKey_ for zero, o identificador de entrada do objeto é simplesmente copiado. 
  
A função **HrComposeEID** permite que os aplicativos trabalhar com objetos em repositórios de vários devido ao uso de identificadores de entrada compostos. Um aplicativo pode chamar a função [HrDecomposeEID](hrdecomposeeid.md) para dividir o identificador de entrada compostos em seus constituintes originais. 
  
## <a name="see-also"></a>Confira também



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

