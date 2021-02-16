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
  
> [in] Um ponteiro para a mensagem à qual o fluxo está associado. Essa mensagem não é necessária para ser a mesma mensagem que é passada na chamada para as funções [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md) 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a interface de fluxo é aberta. Os sinalizadores a seguir podem ser definidos:
    
MAPI_CREATE 
  
> Se uma propriedade não existir na mensagem atual, ela deverá ser criada. Se a propriedade existir, os dados atuais na propriedade deverão ser substituídos com os dados do fluxo Transport-Neutral TNEF (Encapsulation Format). Quando uma implementação define o MAPI_CREATE, ele também deve definir o MAPI_MODIFY sinalizador.
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. A interface padrão é somente leitura. MAPI_MODIFY deve ser definido sempre que MAPI_CREATE definida.
    
 _lppStream_
  
> [out] Um ponteiro para um ponteiro para um objeto de fluxo que contém o texto da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) da mensagem encapsulada passada e que oferece suporte à interface [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::OpenTaggedBody** para abrir uma interface de fluxo no texto de uma mensagem encapsulada (ou seja, em um objeto TNEF). 
  
Como parte de seu processamento, **OpenTaggedBody** insere ou analisado marcas de anexo que indicam a posição de quaisquer anexos ou objetos OLE no texto da mensagem. As marcas de anexo estão no seguinte formato: 
  
 **[[** _nome do anexo_ **:** n _no_ **nome** _do contêiner do anexo_ **]]**
  
 _o nome do_ anexo descreve o objeto attachment;  _n_ é um número que identifica o anexo que faz parte de uma sequência, incrementando do valor passado no parâmetro  _lpKey_ da função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx;](opentnefstreamex.md) e  _o nome do contêiner_ de anexo descreve o componente físico em que o objeto anexo reside. 
  
 **OpenTaggedBody** lê o texto da mensagem e insere uma marca de anexo sempre que um objeto de anexo apareceu originalmente no texto. O texto da mensagem original não é alterado. 
  
Quando uma mensagem com marcas é passada para um fluxo, as marcas são retiradas e os objetos de anexo são realocados na posição das marcas no fluxo.
  
## <a name="see-also"></a>Confira também



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

