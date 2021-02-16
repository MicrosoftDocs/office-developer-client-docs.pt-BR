---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416437"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Processa componentes individuais de uma mensagem, um de cada vez, em um fluxo TNEF (Transport-Neutral Encapsulation Format).
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla qual componente será concluído. Um ou outro dos sinalizadores a seguir deve ser definido:
    
TNEF_COMPONENT_ATTACHMENT 
  
> O processamento será concluído para um objeto de anexo; o  _parâmetro ulComponentID_ contém a **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo. 
    
TNEF_COMPONENT_MESSAGE 
  
> O processamento será concluído para um objeto de mensagem. 
    
 _ulComponentID_
  
> [in] 0 para indicar o processamento de uma mensagem ou a PR_ATTACH_NUM **de** um anexo a ser processado. Se o TNEF_COMPONENT_MESSAGE sinalizador for definido no  _parâmetro ulFlags,_  _ulComponentID_ deverá ser 0. 
    
 _lpCustomPropList_
  
> [in] Um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém marcas de propriedade que identificam as propriedades passadas no _parâmetro lpCustomProps._ Deve haver uma correspondência um-para-um entre cada valor de propriedade em _lpCustomProps_ e uma marca de propriedade no _parâmetro lpCustomPropList._ 
    
 _lpCustomProps_
  
> [in] Um ponteiro para uma [estrutura SPropValue](spropvalue.md) que contém valores de propriedade para as propriedades a codificar. 
    
 _lpPropList_
  
> [in] Um ponteiro para uma **estrutura SPropTagArray** que contém marcas de propriedade para as propriedades a codificar. 
    
 _lppProblems_
  
> [out] Um ponteiro para um ponteiro para uma [estrutura STnefProblemArray](stnefproblemarray.md) retornada. A **estrutura STnefProblemArray** indica quais propriedades, se alguma, não foram codificadas corretamente. Se NULL for passado no parâmetro  _lppProblems,_ nenhuma matriz de problema de propriedade será retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::FinishComponent** para executar o processamento TNEF para um componente, uma mensagem ou um anexo, conforme indicado pelo sinalizador definido no parâmetro _ulFlags._ 
  
Para que o processamento de componentes seja habilitado, o provedor de chamada ou gateway passa o sinalizador TNEF_COMPONENT_ENCODING em  _ulFlags_ para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) que abriu o objeto para receber a codificação. 
  
Passar valores nos parâmetros _lpCustomPropList_ e _lpCustomProps_ executa a codificação de componente equivalente à feita pelo método [ITnef::SetProps.](itnef-setprops.md) Passar um valor no parâmetro  _lpPropList_ executa a codificação de componente equivalente à feita pelo método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE definido em  _ulFlags_. Passar esses valores permite executar codificações com uma única chamada em vez de várias chamadas.
  
A implementação do TNEF relata problemas de codificação de fluxo TNEF sem interromper **o processo FinishComponent.** A **estrutura STnefProblemArray** retornada em  _lppProblems_ indica quais atributos TNEF ou propriedades MAPI, se algum, não puderam ser processados. O valor retornado no membro **scode** de uma das estruturas **STnefProblem** contidas em **STnefProblemArray** indica o problema específico. O provedor ou gateway pode trabalhar na suposição de que todas as propriedades ou atributos para os quais **FinishComponent** não retorna um relatório de problemas foram processados com êxito. 
  
Se um provedor ou gateway não funcionar com matrizes de problemas, ele poderá passar NULL em  _lppProblems_; nesse caso, nenhuma matriz do problema será retornada.
  
O valor retornado em  _lppProblems_ só será válido se a chamada retornar S_OK. Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na [estrutura STnefProblemArray.](stnefproblemarray.md) Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamada ou gateway não deverá usar ou liberar a estrutura. Se não ocorrer nenhum erro na chamada, o provedor de chamada ou gateway deverá liberar a memória para **o STnefProblemArray** chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

