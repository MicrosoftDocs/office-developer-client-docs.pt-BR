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
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435674"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conclui o processamento de todas as operações do formato de encapsulamento de transporte neutro (TNEF) que estão na fila e aguardando. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpKey_
  
> bota Um ponteiro para a propriedade da chave **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo. O objeto de encapsulamento TNEF usa essa chave para corresponder a um anexo à sua marca de posicionamento de anexo em uma mensagem. Essa chave deve ser exclusiva para cada anexo.
    
 _lpProblem_
  
> bota Um ponteiro para um ponteiro para uma estrutura [STnefProblemArray](stnefproblemarray.md) retornada. A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas corretamente. Se NULL for passado no parâmetro _lpProblem_ , nenhuma matriz de problemas de propriedade será retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: Finish** para executar a codificação de todas as propriedades para as quais a codificação foi solicitada em chamadas para os métodos [ITnef::](itnef-addprops.md) addprops e [ITnef:](itnef-setprops.md) : SetProps. Se o objeto TNEF tiver sido aberto com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) , o método **Finish** codificará as propriedades solicitadas no fluxo de encapsulamento passado para esse objeto. Se o objeto TNEF tiver sido aberto com o sinalizador TNEF_DECODE, o método **Finalize** decodificará as propriedades do fluxo TNEF e as gravará novamente na mensagem à qual pertencem. 
  
Após a chamada de **término** , o ponteiro para o fluxo de encapsulamento aponta para o final dos dados TNEF. Se o provedor ou gateway precisar usar os dados de fluxo TNEF após a chamada de **término** , ele deverá redefinir o ponteiro de fluxo para o início dos dados de fluxo TNEF. 
  
A implementação TNEF relata os problemas de codificação de fluxo TNEF sem interromper o processo de **conclusão** . A estrutura [STnefProblemArray](stnefproblemarray.md) retornada no parâmetro _lpProblem_ indica quais atributos do TNEF ou propriedades MAPI, se houver, não puderam ser processados. O valor retornado no membro **SCODE** de uma das estruturas **STnefProblem** contidas no **STnefProblemArray** indica o problema específico. O provedor ou gateway pode funcionar na pressuposição de que todas as propriedades ou atributos para os quais **concluir** não retornar um relatório de problemas foram processados com êxito. 
  
Se um provedor ou gateway não funcionar com matrizes problemáticas, ele poderá passar NULL no _lpProblem_; Nesse caso, nenhum conjunto de problemas é retornado. 
  
O valor retornado em _lpProblem_ é válido somente se a chamada retornar S_OK. Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** . Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamadas ou o gateway não deverá usar ou liberar a estrutura. Se nenhum erro ocorrer na chamada, o provedor de chamada ou o gateway deve liberar a memória para o **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Arquivo. cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa o método **ITnef:: Finish** para concluir o processamento do novo fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

