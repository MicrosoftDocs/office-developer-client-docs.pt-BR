---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348619"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o provedor de serviços de chamada ou o gateway adicione Propriedades ao encapsulamento de uma mensagem ou de um anexo. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como as propriedades são incluídas ou excluídas do encapsulamento. Os seguintes sinalizadores podem ser definidos:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codifica apenas as propriedades no parâmetro _lpPropList_ que fazem parte dos anexos na mensagem. 
    
TNEF_PROP_CONTAINED 
  
> Codifica apenas as propriedades do anexo especificado pelo parâmetro _ulElemID_ . Se o parâmetro _lpvData_ não for NULL, os dados apontados serão gravados no encapsulamento do anexo no arquivo indicado pela propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codifica somente as propriedades da mensagem ou do anexo especificado pelo parâmetro _ulElemID_ . Se esse sinalizador estiver definido, o valor em _lpvData_ deve ser um ponteiro de [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
TNEF_PROP_EXCLUDE 
  
> Codifica todas as propriedades não especificadas no parâmetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Codifica todas as propriedades especificadas em _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codifica apenas as propriedades especificadas no _lpPropList_ que fazem parte da própria mensagem. 
    
 _ulElemID_
  
> no A propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número que identifica exclusivamente o anexo em sua mensagem pai. O parâmetro _ulElemID_ é usado quando a manipulação especial é solicitada para um anexo. O parâmetro _ulElemID_ deve ser 0, a menos que o sinalizador TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpvData_
  
> no Um ponteiro para dados de anexo usados para substituir os dados do anexo especificado em _ulElemID_. O parâmetro _lpvData_ deve ser NULL, a não ser que TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF esteja definido em _parâmetroulflags_.
    
 _lpPropList_
  
> no Um ponteiro para a lista de propriedades para incluir ou excluir do encapsulamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef::** addprops para listar as propriedades a serem incluídas ou excluídas do processamento TNEF (Transport-neutral Encapsulation Format) de uma mensagem ou de um anexo. Usando as chamadas sucessivas, o provedor ou gateway pode especificar uma lista de propriedades a serem adicionadas e codificadas ou excluídas da codificação. Provedores e gateways também podem usar **** addprops para fornecer informações sobre anexos de tratamento especial. 
  
 **** Addprops tem suporte apenas para objetos TNEF que são abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Observe que nenhuma codificação TNEF real acontece para **** addprops até que o método [ITnef:: Finish](itnef-finish.md) seja chamado. Essa funcionalidade significa que os ponteiros **** passados para addprops devem permanecer válidos até que a chamada para **término** seja feita. Nesse ponto, todos os objetos e dados passados com as **** chamadas addprops podem ser liberados ou liberados. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Arquivo. cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa o método **ITnef::** addprops para copiar as propriedades de uma mensagem para um fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

