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
  
Permite que o provedor de serviços de chamada ou gateway adicione propriedades ao encapsulamento de uma mensagem ou anexo. 
  
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
  
> [in] Uma bitmask de sinalizadores que controla como as propriedades são incluídas ou excluídas do encapsulamento. Os sinalizadores a seguir podem ser definidos:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codifica somente as propriedades no  _parâmetro lpPropList_ que fazem parte dos anexos na mensagem. 
    
TNEF_PROP_CONTAINED 
  
> Codifica somente as propriedades do anexo especificado pelo _parâmetro ulElemID._ Se o parâmetro  _lpvData_ não for NULL, os dados apontados serão gravados no encapsulamento do anexo no arquivo indicado pela propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codifica somente as propriedades da mensagem ou do anexo especificados pelo _parâmetro ulElemID._ Se esse sinalizador estiver definido, o valor em _lpvData_ deverá ser um [ponteiro IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
TNEF_PROP_EXCLUDE 
  
> Codifica todas as propriedades não especificadas no _parâmetro lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Codifica todas as propriedades especificadas em  _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codifica somente as propriedades especificadas em  _lpPropList_ que fazem parte da mensagem em si. 
    
 _ulElemID_
  
> [in] A propriedade **PR_ATTACH_NUM** de um anexo ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), que contém um número que identifica exclusivamente o anexo em sua mensagem pai. O  _parâmetro ulElemID_ é usado quando uma manipulação especial é solicitada para um anexo. O _parâmetro ulElemID_ deve ser 0, a menos que o sinalizador TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF seja definido no _parâmetro ulFlags._ 
    
 _lpvData_
  
> [in] Um ponteiro para dados de anexo usados para substituir os dados do anexo especificado em  _ulElemID_. O  _parâmetro lpvData_ deve ser NULL, a menos que TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF seja definido em  _ulFlags_.
    
 _lpPropList_
  
> [in] Um ponteiro para a lista de propriedades a incluir ou excluir do encapsulamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::AddProps** para listar propriedades a serem incluídas ou excluídas do processamento de formato de encapsulamento Transport-Neutral (TNEF) de uma mensagem ou um anexo. Usando chamadas sucessivas, o provedor ou gateway pode especificar uma lista de propriedades para adicionar e codificar ou excluir da codificação. Os provedores e gateways também podem usar **AddProps** para fornecer informações sobre qualquer tratamento especial de anexos que devem ser dados. 
  
 **AddProps** é suportado apenas para objetos TNEF que são abertos com o sinalizador TNEF_ENCODE para as funções [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Observe que nenhuma codificação TNEF real acontece para **AddProps** até que o método [ITnef::Finish](itnef-finish.md) seja chamado. Essa funcionalidade significa que os ponteiros passados para **AddProps** devem permanecer válidos até que a chamada para **Concluir** seja feita. Nesse ponto, todos os objetos e dados passados com **chamadas AddProps** podem ser liberados ou liberados. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa o **método ITnef::AddProps** para copiar propriedades de uma mensagem para um fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

