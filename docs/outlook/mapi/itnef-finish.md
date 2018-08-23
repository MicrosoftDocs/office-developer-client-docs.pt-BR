---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583761"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tiver terminado de processamento de todas as operações de Transport-Neutral Encapsulation Format (TNEF) que estão enfileiradas e em espera. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpKey_
  
> [out] Um ponteiro para a propriedade de chave **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo. O objeto de encapsulamento TNEF usa essa chave para coincidir com um anexo para sua tag de posicionamento de anexo em uma mensagem. Essa chave deve ser exclusivo para cada anexo.
    
 _lpProblem_
  
> [out] Um ponteiro para um ponteiro para uma estrutura de [STnefProblemArray](stnefproblemarray.md) retornado. A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas adequadamente. Se NULL é passada no parâmetro _lpProblem_ , nenhuma matriz de problema da propriedade será retornado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Chamada de gateways, o método **ITnef::Finish** para executar a codificação de todas as propriedades para a qual codificação foi solicitado em chamadas para os métodos [ITnef::AddProps](itnef-addprops.md) e [ITnef::SetProps](itnef-setprops.md) , provedores de armazenamento de mensagem e provedores de transporte. Se o objeto TNEF foi aberto com o sinalizador TNEF_ENCODE para a função [OpenTnefStreamEx](opentnefstreamex.md) ou [OpenTnefStream](opentnefstream.md) , o método **término** codifica as propriedades solicitadas no fluxo encapsulamento passado para esse objeto. Se o objeto TNEF foi aberto com o sinalizador TNEF_DECODE, o método **término** decodifica as propriedades do fluxo de TNEF e grava-os de volta à mensagem que pertencem. 
  
Após a chamada de **término** , o ponteiro para o fluxo de encapsulamento aponta para o final dos dados TNEF. Se o provedor ou o gateway precisa usar os dados de fluxo TNEF após o **término** de chamada, ele deverá redefinir o ponteiro do fluxo ao início dos dados stream TNEF. 
  
A implementação de TNEF relata problemas de codificação de fluxo TNEF sem interromper o processamento de **término** . A estrutura de [STnefProblemArray](stnefproblemarray.md) retornada no parâmetro _lpProblem_ indica quais atributos TNEF ou propriedades MAPI, se houver, não pôde ser processadas. O valor retornado no membro **scode** um das estruturas **STnefProblem** contidos no **STnefProblemArray** indica que o problema específico. O provedor ou o gateway pode trabalhar no pressuposto de que todas as propriedades ou os atributos para os quais a **Concluir** , não retorna um relatório de problema foram processados com êxito. 
  
Se um provedor ou gateway não funciona com matrizes de problema, ele pode passar NULL em _lpProblem_; Nesse caso, a matriz nenhum problema é retornado. 
  
O valor retornado em _lpProblem_ é válido somente se a chamada Retorna S_OK. Quando for retornado S_OK, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** . Se ocorrer um erro na chamada, a estrutura de **STnefProblemArray** não for preenchida e o gateway ou provedor de chamada não deve usar ou livre a estrutura. Se nenhum erro ocorrer na chamada, o provedor de chamada ou gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|CPP  <br/> |SaveToTNEF  <br/> |MFCMAPI usa o método **ITnef::Finish** para concluir o processamento do novo fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

