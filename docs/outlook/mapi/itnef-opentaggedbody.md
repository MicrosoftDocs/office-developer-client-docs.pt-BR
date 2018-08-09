---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ed433dc1fcf2a366d2ece07ac06d4e12558e4aa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767721"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Aplica-se a**: Outlook 
  
Abre uma interface de fluxo no texto de uma mensagem encapsulado.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> [in] Um ponteiro para a mensagem com a qual o stream está associado. Esta mensagem não é necessária para ser a mesma mensagem que é passada na chamada para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a interface do fluxo é aberta. Sinalizadores a seguir podem ser definidos:
    
MAPI_CREATE 
  
> Se uma propriedade não existir na mensagem atual, ele deve ser criado. Se a propriedade existir, os dados atuais na propriedade devem ser substituídos com os dados do fluxo de Transport-Neutral Encapsulation Format (TNEF). Quando uma implementação define o sinalizador MAPI_CREATE, ele também deve definir o sinalizador MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. A interface padrão é somente leitura. MAPI_MODIFY deve ser definida sempre que MAPI_CREATE é definida.
    
 _lppStream_
  
> [out] Um ponteiro para um ponteiro para um objeto stream que contém o texto da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de passados-in encapsulado mensagem e que dá suporte à interface [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagem e gateways chame o método de **ITnef::OpenTaggedBody** para abrir uma interface de fluxo no texto de uma mensagem encapsulado (ou seja, um TNEF do objeto). 
  
Como parte do seu processamento, **OpenTaggedBody** insere ou analisa as marcas de anexo que indicam a posição de todos os anexos ou objetos OLE no texto da mensagem. As marcas de anexo são no seguinte formato: 
  
 **[[** o _nome do anexo_ **:** _n_ **no** _nome do contêiner de anexo_ **]]**
  
 _nome do anexo_ descreve o objeto de anexo;  _n_ é um número que identifica o anexo que faz parte de uma sequência, incrementar do valor passado no parâmetro _lpKey_ do [OpenTnefStream](opentnefstream.md) ou função [OpenTnefStreamEx](opentnefstreamex.md) ; e _o nome de contêiner de anexo_ descreve o componente físico onde o objeto de anexo reside. 
  
 **OpenTaggedBody** lê o texto de mensagem e insere uma marca de anexo sempre que um objeto attachment aparecia originalmente no texto. O texto da mensagem original não é alterado. 
  
Quando uma mensagem que tenha marcas é passada para um stream, as marcas serão perdidas e os objetos attachment contidos forem realocados na posição das marcas no stream.
  
## <a name="see-also"></a>Confira também



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

