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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348731"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma interface de fluxo no texto de uma mensagem encapsulada.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parâmetros

 _lpMessage_
  
> no Um ponteiro para a mensagem à qual o Stream está associado. Esta mensagem não precisa ser a mesma mensagem que é passada na chamada para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a interface de fluxo é aberta. Os seguintes sinalizadores podem ser definidos:
    
MAPI_CREATE 
  
> Se uma propriedade não existir na mensagem atual, ela deverá ser criada. Se a propriedade existir, os dados atuais da propriedade deverão ser substituídos pelos dados do fluxo TNEF (Transport-neutral Encapsulation Format). Quando uma implementação define o sinalizador MAPI_CREATE, ela também deve definir o sinalizador MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. A interface padrão é somente leitura. MAPI_MODIFY deve ser definido sempre que MAPI_CREATE estiver definido.
    
 _lppStream_
  
> bota Um ponteiro para um ponteiro para um objeto Stream que contém o texto da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) da mensagem encapsulada aprovada e que oferece suporte à interface [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: OpenTaggedBody** para abrir uma interface de fluxo no texto de uma mensagem encapsulada (ou seja, em um objeto TNEF). 
  
Como parte do seu processamento, o **OpenTaggedBody** insere ou analisa marcas de anexo que indicam a posição de qualquer anexo ou objeto OLE no texto da mensagem. As marcas de anexo estão no seguinte formato: 
  
 **[[** _nome do anexo_ **:** _n_ **no nome do contêiner de** _anexo_ **]]**
  
 _nome do anexo_ descreve o objeto Attachment;  _n_ é um número que identifica o anexo que faz parte de uma sequência, incrementando do valor passado no parâmetro _LpKey_ da função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) ; e _nome do contêiner de anexo_ descreve o componente físico onde reside o objeto Attachment. 
  
 O **OpenTaggedBody** lê o texto da mensagem e insere uma marca de anexo em qualquer lugar em que um objeto Attachment apareceu originalmente no texto. O texto da mensagem original não é alterado. 
  
Quando uma mensagem que tem marcas é passada para um fluxo, as marcas são removidas e os objetos Attachment são realocados na posição das marcas no Stream.
  
## <a name="see-also"></a>Confira também



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

