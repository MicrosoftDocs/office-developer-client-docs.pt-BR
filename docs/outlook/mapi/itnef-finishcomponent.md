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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278883"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Processa componentes individuais de uma mensagem de cada vez em um fluxo TNEF (Transport-neutral Encapsulation Format).
  
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
  
> no Uma bitmask de sinalizadores que controla qual componente será concluído. Um ou outro dos seguintes sinalizadores devem ser definidos:
    
TNEF_COMPONENT_ATTACHMENT 
  
> O processamento será concluído para um objeto Attachment; o parâmetro _ulComponentID_ contém a propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo. 
    
TNEF_COMPONENT_MESSAGE 
  
> O processamento será concluído para um objeto Message. 
    
 _ulComponentID_
  
> [in] 0 para indicar o processamento de uma mensagem ou a propriedade **PR_ATTACH_NUM** de um anexo a ser processada. Se o sinalizador TNEF_COMPONENT_MESSAGE estiver definido no parâmetro _parâmetroulflags_ , _ulComponentID_ deverá ser 0. 
    
 _lpCustomPropList_
  
> no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade que identificam as propriedades passadas no parâmetro _lpCustomProps_ . Deve haver uma correspondência de um para um entre cada valor de propriedade no _lpCustomProps_ e uma marca de propriedade no parâmetro _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> no Um ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém valores de propriedade para as propriedades a serem codificadas. 
    
 _lpPropList_
  
> no Um ponteiro para uma estrutura **SPropTagArray** que contém as marcas de propriedade para as propriedades a serem codificadas. 
    
 _lppProblems_
  
> bota Um ponteiro para um ponteiro para uma estrutura [STnefProblemArray](stnefproblemarray.md) retornada. A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas corretamente. Se NULL for passado no parâmetro _lppProblems_ , nenhuma matriz de problemas de propriedade será retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: FinishComponent** para executar o processamento TNEF para um componente, uma mensagem ou um anexo, conforme indicado pelo sinalizador definido no parâmetro _parâmetroulflags_ . 
  
Para que o processamento de componentes seja habilitado, o provedor de chamadas ou o gateway passe o sinalizador TNEF_COMPONENT_ENCODING no _parâmetroulflags_ para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) que abriu o objeto para receber a codificação. 
  
Passar valores nos parâmetros _lpCustomPropList_ e _lpCustomProps_ executa a codificação de componente equivalente a isso feito pelo método [ITnef::](itnef-setprops.md) SetProps. Passar um valor no parâmetro _lpPropList_ realiza a codificação do componente equivalente a feita pelo método [ITnef::](itnef-addprops.md) addprops com o sinalizador TNEF_PROP_INCLUDE definido em _parâmetroulflags_. Passar esses valores permite que você execute codificações com uma única chamada em vez de várias chamadas.
  
A implementação TNEF relata os problemas de codificação de fluxo TNEF sem interromper o processo **FinishComponent** . A estrutura **STnefProblemArray** retornada no _lppProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não puderam ser processados. O valor retornado no membro **SCODE** de uma das estruturas **STnefProblem** contidas no **STnefProblemArray** indica o problema específico. O provedor ou gateway pode funcionar na pressuposição de que todas as propriedades ou atributos para os quais o **FinishComponent** não retorna um relatório de problemas foram processados com êxito. 
  
Se um provedor ou gateway não funcionar com matrizes problemáticas, ele poderá passar NULL no _lppProblems_; Nesse caso, nenhum conjunto de problemas é retornado.
  
O valor retornado em _lppProblems_ é válido somente se a chamada retornar S_OK. Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na estrutura [STnefProblemArray](stnefproblemarray.md) . Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamadas ou o gateway não deverá usar ou liberar a estrutura. Se nenhum erro ocorrer na chamada, o provedor de chamada ou o gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

