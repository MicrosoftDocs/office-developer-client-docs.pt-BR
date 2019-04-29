---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430788"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o valor de uma ou mais propriedades de uma mensagem encapsulada ou anexo sem modificar a mensagem original ou o anexo. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como os valores de propriedade são definidos. O seguinte sinalizador pode ser definido:
    
TNEF_PROP_CONTAINED 
  
> Codifica somente as propriedades da mensagem ou do anexo especificado pelo parâmetro _ulElemID_ . 
    
 _ulElemID_
  
> no A propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número que identifica exclusivamente o anexo em sua mensagem pai.
    
 _cValues_
  
> no O número de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontados pelo parâmetro _lpProps_ . 
    
 _lpProps_
  
> no Um ponteiro para uma estrutura **SPropValue** que contém os valores de propriedade das propriedades a serem definidos. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef::** SetProps para definir propriedades a serem incluídas no encapsulamento de uma mensagem ou anexo sem modificar a mensagem original ou o anexo. Todas as propriedades definidas com essa chamada substituem as propriedades existentes na mensagem encapsulada. 
  
 **** SetProps tem suporte apenas para objetos TNEF que são abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . Qualquer número de propriedades pode ser definido com esta chamada. 
  
> [!NOTE]
> Nenhuma codificação TNEF real para **** SetProps acontece até após o método [ITnef:: Finish](itnef-finish.md) ser chamado. Essa funcionalidade significa que os ponteiros **** passados para SetProps devem permanecer válidos até que a chamada para **término** seja feita. Nesse ponto, todos os objetos e dados passados para **** as chamadas de SetProps podem ser liberados ou liberados. 
  
## <a name="see-also"></a>Confira também



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

