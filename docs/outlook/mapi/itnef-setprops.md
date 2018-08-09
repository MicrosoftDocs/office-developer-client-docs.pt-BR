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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767730"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**Aplica-se a**: Outlook 
  
Define o valor de uma ou mais propriedades para uma mensagem encapsulada ou um anexo sem modificar a mensagem original ou um anexo. 
  
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
  
> [in] Uma bitmask dos sinalizadores que controla como os valores de propriedade são definidos. O seguinte sinalizador pode ser definido:
    
TNEF_PROP_CONTAINED 
  
> Codifica apenas as propriedades da mensagem ou anexo especificado pelo parâmetro _ulElemID_ . 
    
 _ulElemID_
  
> [in] Propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número de forma exclusiva identifica o anexo na mensagem de seu pai.
    
 _cValues_
  
> [in] O número de valores de propriedade na estrutura [SPropValue](spropvalue.md) apontado pelo parâmetro _lpProps_ . 
    
 _lpProps_
  
> [in] Um ponteiro para uma estrutura **SPropValue** que contém os valores de propriedade para definir as propriedades. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Provedores, provedores de armazenamento de mensagem e o método **ITnef::SetProps** de chamada de gateways para definir propriedades para incluir no encapsulamento de uma mensagem ou um anexo sem modificar a mensagem original ou um anexo de transporte. Todas as propriedades definidas com esta chamada substituiem propriedades existentes na mensagem encapsulada. 
  
 **SetProps** é suportado somente para os objetos TNEF abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . Qualquer número de propriedades pode ser definido com esta chamada. 
  
> [!NOTE]
> Nenhuma codificação TNEF real para **SetProps** acontece até depois que o método [ITnef::Finish](itnef-finish.md) é chamado. Essa funcionalidade significa que os ponteiros passados para **SetProps** devem permanecer válidos até após a chamada para **Concluir a** é feita. Nesse momento, todos os objetos e dados passados para **SetProps** chamadas podem ser lançados ou liberados. 
  
## <a name="see-also"></a>Confira também



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

