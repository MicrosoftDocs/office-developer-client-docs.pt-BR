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
  
Define o valor de uma ou mais propriedades para uma mensagem ou anexo encapsulado sem modificar a mensagem ou o anexo original. 
  
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
  
> [in] Uma bitmask de sinalizadores que controla como os valores de propriedade são definidos. O sinalizador a seguir pode ser definido:
    
TNEF_PROP_CONTAINED 
  
> Codifica somente as propriedades da mensagem ou do anexo especificado pelo _parâmetro ulElemID._ 
    
 _ulElemID_
  
> [in] A propriedade **PR_ATTACH_NUM** de um anexo ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), que contém um número que identifica exclusivamente o anexo em sua mensagem pai.
    
 _cValues_
  
> [in] O número de valores de propriedade na [estrutura SPropValue](spropvalue.md) apontado pelo parâmetro _lpProps._ 
    
 _lpProps_
  
> [in] Um ponteiro para uma **estrutura SPropValue** que contém os valores de propriedade das propriedades a definir. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::SetProps** para definir propriedades a incluir no encapsulamento de uma mensagem ou anexo sem modificar a mensagem ou anexo original. Todas as propriedades definidas com essa chamada substituem as propriedades existentes na mensagem encapsulada. 
  
 **SetProps** é suportado apenas para objetos TNEF que são abertos com o sinalizador TNEF_ENCODE para as funções [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md) Qualquer número de propriedades pode ser definido com essa chamada. 
  
> [!NOTE]
> Nenhuma codificação TNEF real para **SetProps** acontece até que o método [ITnef::Finish](itnef-finish.md) seja chamado. Essa funcionalidade significa que os ponteiros passados para **SetProps** devem permanecer válidos até que a chamada para **Concluir** seja feita. Nesse ponto, todos os objetos e dados passados para chamadas **SetProps** podem ser liberados ou liberados. 
  
## <a name="see-also"></a>Confira também



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

