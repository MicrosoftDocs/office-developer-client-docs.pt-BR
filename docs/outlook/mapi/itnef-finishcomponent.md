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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7008549111f1b914cf2025c8d61ebc07196706fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767727"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Aplica-se a**: Outlook 
  
Processa os componentes individuais de uma mensagem de um por vez em um fluxo de Transport-Neutral Encapsulation Format (TNEF).
  
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
  
> [in] Uma bitmask dos sinalizadores que controla o componente que vai ser concluída. Um ou outro dos sinalizadores a seguir deve ser definido:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Processamento será concluído para um objeto attachment; o parâmetro _ulComponentID_ contém a propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo. 
    
TNEF_COMPONENT_MESSAGE 
  
> Processamento vai ser concluído para um objeto de mensagem. 
    
 _ulComponentID_
  
> [in] 0 para indicar o processamento de uma mensagem ou a propriedade **PR_ATTACH_NUM** de um anexo a ser processado. Se o sinalizador TNEF_COMPONENT_MESSAGE é definido no parâmetro _ulFlags_ , _ulComponentID_ deve ser 0. 
    
 _lpCustomPropList_
  
> [in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém marcas de propriedade que identificam as propriedades passada no parâmetro _lpCustomProps_ . Deve haver uma correspondência direta entre cada valor de propriedade em _lpCustomProps_ e uma marca de propriedade no parâmetro _lpCustomPropList_ . 
    
 _lpCustomProps_
  
> [in] Um ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém os valores de propriedade para as propriedades codificar. 
    
 _lpPropList_
  
> [in] Um ponteiro para uma estrutura **SPropTagArray** que contém marcas de propriedade para as propriedades codificar. 
    
 _lppProblems_
  
> [out] Um ponteiro para um ponteiro para uma estrutura de [STnefProblemArray](stnefproblemarray.md) retornado. A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas adequadamente. Se NULL é passada no parâmetro _lppProblems_ , nenhuma matriz de problema da propriedade será retornado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Transporte provedores, provedores de armazenamento de mensagem e o método **ITnef::FinishComponent** de chamada de gateways para executar o TNEF processamento para um componente, uma mensagem ou um anexo, conforme indicado pelo sinalizador definido no parâmetro _ulFlags_ . 
  
Para processamento de componente a ser habilitada, o provedor de chamada ou gateway passar o sinalizador TNEF_COMPONENT_ENCODING _ulFlags_ para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) que abriu o objeto para receber a codificação. 
  
Passando valores nos parâmetros _lpCustomPropList_ e _lpCustomProps_ executa componente codificação equivalente à que feito pelo método [ITnef::SetProps](itnef-setprops.md) . Passando um valor no parâmetro _lpPropList_ executa o equivalente de codificação de componente que feito pelo método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE definido em _ulFlags_. Passar esses valores, permite que você execute codificações com uma única chamada em vez de várias chamadas.
  
A implementação de TNEF relata problemas de codificação de fluxo TNEF sem interromper o processamento de **FinishComponent** . A estrutura de **STnefProblemArray** retornada em _lppProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não pôde ser processadas. O valor retornado no membro **scode** um das estruturas **STnefProblem** contidos no **STnefProblemArray** indica que o problema específico. O provedor ou o gateway pode trabalhar no pressuposto de que todas as propriedades ou os atributos para os quais **FinishComponent** não retorna um relatório de problema foram processados com êxito. 
  
Se um provedor ou gateway não funciona com matrizes de problema, ele pode passar NULL em _lppProblems_; Nesse caso, a matriz nenhum problema é retornado.
  
O valor retornado em _lppProblems_ é válido somente se a chamada Retorna S_OK. Quando for retornado S_OK, o provedor ou gateway deve verificar os valores retornados na estrutura [STnefProblemArray](stnefproblemarray.md) . Se ocorrer um erro na chamada, a estrutura de **STnefProblemArray** não for preenchida e o gateway ou provedor de chamada não deve usar ou livre a estrutura. Se nenhum erro ocorrer na chamada, o provedor de chamada ou gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

