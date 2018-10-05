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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396313"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que o provedor de serviços de chamada ou gateway adicionar propriedades ao encapsulamento de uma mensagem ou um anexo. 
  
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
  
> [in] Uma bitmask dos sinalizadores que controla como propriedades são incluídas em ou excluídas de encapsulamento. Sinalizadores a seguir podem ser definidos:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codifica apenas as propriedades no parâmetro _lpPropList_ que fazem parte de anexos da mensagem. 
    
TNEF_PROP_CONTAINED 
  
> Codifica apenas as propriedades do anexo especificado pelo parâmetro _ulElemID_ . Se o parâmetro _lpvData_ não for nulo, os dados apontados são gravados para encapsulamento do anexo no arquivo indicado pela propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codifica apenas as propriedades da mensagem ou anexo especificado pelo parâmetro _ulElemID_ . Se esse sinalizador estiver definido, o valor em _lpvData_ deve ser um ponteiro [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
TNEF_PROP_EXCLUDE 
  
> Codifica todas as propriedades não especificadas no parâmetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Codifica todas as propriedades especificadas na _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codifica apenas as propriedades especificadas na _lpPropList_ que fazem parte da mensagem em si. 
    
 _ulElemID_
  
> [in] Propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo, que contém um número de forma exclusiva identifica o anexo na mensagem de seu pai. O parâmetro _ulElemID_ é usado quando a ação especial é solicitada para um anexo. O parâmetro _ulElemID_ deve ser 0 a menos que o sinalizador TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF é definido no parâmetro _ulFlags_ . 
    
 _lpvData_
  
> [in] Um ponteiro para dados de anexo usados para substituir os dados do anexo especificado em _ulElemID_. O parâmetro _lpvData_ deve ser NULL, a menos que TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF está definida na _ulFlags_.
    
 _lpPropList_
  
> [in] Um ponteiro para a lista de propriedades para incluir ou excluir do encapsulamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagem e gateways chame o método de **ITnef::AddProps** às propriedades de lista para ser incluídos ou excluídos do processamento de uma mensagem ou um anexo Transport-Neutral Encapsulation Format (TNEF). Usando sucessivas chamadas, o provedor ou o gateway pode especificar uma lista de propriedades para adicionar e codificar ou excluídos da sendo codificado. Provedores e gateways também podem usar **AddProps** para fornecer informações sobre todos os anexos manipulação especial devem ser dada. 
  
 **AddProps** é suportado somente para os objetos TNEF abertos com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Observe que nenhuma real a codificação TNEF acontece para **AddProps** até que o método [ITnef::Finish](itnef-finish.md) é chamado. Essa funcionalidade significa que os ponteiros passados para **AddProps** devem permanecer válidos até após a chamada para **Concluir a** é feita. Nesse momento, todos os objetos e dados passados com **AddProps** chamadas podem ser lançados ou liberados. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|CPP  <br/> |SaveToTNEF  <br/> |MFCMAPI usa o método **ITnef::AddProps** para copiar propriedades de uma mensagem para um fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

