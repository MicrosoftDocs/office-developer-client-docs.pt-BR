---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 26949f10e22c4d2ea49594ee3365ae7d3bb3662d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767739"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Aplica-se a**: Outlook 
  
Extrai as propriedades de um encapsulamento TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como as propriedades são decodificadas. Sinalizadores a seguir podem ser definidos:
    
TNEF_PROP_EXCLUDE 
  
> Decodifica todas as propriedades não especificadas no parâmetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Decodifica todas as propriedades especificadas na _lpPropList_.
    
 _lpPropList_
  
> [in] Um ponteiro para a lista de propriedades para incluir ou excluir a partir da operação de decodificação.
    
 _lpProblems_
  
> [out] Um ponteiro para um ponteiro para uma estrutura de [STnefProblemArray](stnefproblemarray.md) retornado. A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas adequadamente. Se NULL é passada no parâmetro _lpProblems_ , nenhuma matriz de problema da propriedade será retornado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_CORRUPT_DATA 
  
> Sendo decodificados em um fluxo de dados estão corrompidos.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagem e gateways chamar o método **ITnef::ExtractProps** para extrair (isto é, decodificar) propriedades a partir do encapsulamento de uma mensagem ou um anexo que foi passado para a função [OpenTnefStream](opentnefstream.md) . O provedor ou gateway de chamada pode especificar uma lista de propriedades para decodificar. Provedores e gateways também podem usar **ExtractProps** para fornecer informações sobre qualquer ação especial para anexos. 
  
 **ExtractProps** preenche a mensagem original passada para **OpenTnefStream** com as propriedades decodificadas. As chamadas subsequentes **ExtractProps** voltar à mensagem e extraia a nova lista de propriedades. 
  
Ao contrário do método [ITnef::AddProps](itnef-addprops.md) , qual filas solicitada ações até que o método **ITnef::Finish** é chamado, o método **ExtractProps** decodifica as propriedades encapsuladas imediatamente quando for chamado. Por esse motivo, a mensagem de destino para decodificação encapsulamento deve ser relativamente vazia. As propriedades existentes na mensagem de destino são substituídas pelas propriedades encapsuladas. 
  
 **ExtractProps** é suportado somente para os objetos que são abertos com o sinalizador TNEF_DECODE para a função **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
A implementação de TNEF relata problemas de codificação de fluxo TNEF sem interromper o processamento de **ExtractProps** . A estrutura de [STnefProblemArray](stnefproblemarray.md) retornada em _lpProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não pôde ser processadas. O valor retornado no membro **scode** um das estruturas **STnefProblem** contidos no **STnefProblemArray** indica que o problema específico. O provedor ou o gateway pode trabalhar no pressuposto de que todas as propriedades ou os atributos para os quais **ExtractProps** não retorna um relatório de problema foram processados com êxito. 
  
> [!NOTE]
> Se uma propriedade no bloco de encapsulamento MAPI não pode ser processada e deixa o fluxo confiável durante a decodificação de um stream TNEF, decodificação do bloco de encapsulamento é interrompido e for informado um problema. A matriz de problema para esse tipo de problema contém L 0 para o membro **ulPropTag** , `attMAPIProps` ou `attAttachment` para o membro **ulAttribute** e MAPI_E_UNABLE_TO_COMPLETE para o membro **scode** . Observe que a decodificação do fluxo não é interrompidas, apenas a decodificação do bloco de encapsulamento de MAPI. O fluxo de decodificação continua com o próximo bloco de atributo. 
  
Se um provedor ou gateway não funciona com matrizes de problema, ele pode passar NULL em _lppProblems_; Nesse caso, a matriz nenhum problema é retornado. 
  
O valor retornado em _lpProblems_ é válido somente se a chamada Retorna S_OK. Quando for retornado S_OK, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** . Se ocorrer um erro na chamada, a estrutura de **STnefProblemArray** não for preenchida e o gateway ou provedor de chamada não deve usar ou livre a estrutura. Se nenhum erro ocorrer na chamada, o provedor de chamada ou gateway deve liberar a memória para a estrutura **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

