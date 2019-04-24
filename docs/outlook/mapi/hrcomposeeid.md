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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348059"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador de entrada composto para um objeto, geralmente uma mensagem em um repositório de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
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
  
> no Ponteiro para a sessão em uso pelo aplicativo cliente. 
    
 _cbStoreRecordKey_
  
> no Tamanho, em bytes, da chave de registro do repositório de mensagens que contém a mensagem ou outro objeto. Se zero for passado no parâmetro _cbStoreRecordKey_ , o parâmetro _ppEID_ apontará para uma cópia do identificador de entrada do objeto. 
    
 _pStoreRecordKey_
  
> no Ponteiro para a chave de registro do repositório de mensagens que contém a mensagem ou outro objeto. 
    
 _cbMsgEID_
  
> no Tamanho, em bytes, do identificador de entrada da mensagem ou de outro objeto. 
    
 _pMsgEID_
  
> no Ponteiro para o identificador de entrada do objeto. 
    
 _pcbEID_
  
> bota Ponteiro para o tamanho, em bytes, do identificador retornado. 
    
 _ppEID_
  
> bota Ponteiro para um ponteiro para o identificador de entrada retornado. Se o valor do parâmetro _cbStoreRecordKey_ for maior que zero, o parâmetro _ppEID_ apontará para um ponteiro para o identificador de entrada composta que é criado. Se _cbStoreRecordKey_ for zero, _ppEID_ apontará para um ponteiro para uma cópia do identificador de entrada do objeto. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Se a mensagem ou outro objeto para o qual o identificador de entrada composta estiver sendo criado residir em um repositório de mensagens, o identificador será criado a partir do identificador de entrada do objeto e da chave de registro da loja. Se o objeto não estiver em um repositório, ou seja, se a contagem de bytes para a chave de registro de repositório passada no _cbStoreRecordKey_ for zero, o identificador de entrada do objeto será simplesmente copiado. 
  
A função **HrComposeEID** permite que os aplicativos trabalhem com objetos em vários repositórios por meio do uso de identificadores de entrada compostos. Um aplicativo pode chamar a função [HrDecomposeEID](hrdecomposeeid.md) para dividir o identificador de entrada composta em seus constituintes originais. 
  
## <a name="see-also"></a>Confira também



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

