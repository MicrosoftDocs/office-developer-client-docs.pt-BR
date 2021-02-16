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
  
Finaliza o processamento de todas as Transport-Neutral TNEF (Formato de Encapsulamento) que estão em fila e aguardando. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpKey_
  
> [out] Um ponteiro para a **PR_ATTACH_NUM** chave ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um anexo. O objeto de encapsulamento TNEF usa essa chave para corresponder a um anexo à marca de posicionamento do anexo em uma mensagem. Essa chave deve ser exclusiva para cada anexo.
    
 _lpProblem_
  
> [out] Um ponteiro para um ponteiro para uma [estrutura STnefProblemArray](stnefproblemarray.md) retornada. A **estrutura STnefProblemArray** indica quais propriedades, se alguma, não foram codificadas corretamente. Se NULL for passado no  _parâmetro lpProblem,_ nenhuma matriz de problema de propriedade será retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::Finish** para executar a codificação de todas as propriedades para as quais a codificação foi solicitada em chamadas para os métodos [ITnef::AddProps](itnef-addprops.md) e [ITnef::SetProps.](itnef-setprops.md) Se o objeto TNEF foi aberto com o sinalizador TNEF_ENCODE para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx,](opentnefstreamex.md) o método **Finish** codifica as propriedades solicitadas no fluxo de encapsulamento passado para esse objeto. Se o objeto TNEF tiver sido aberto com o sinalizador TNEF_DECODE, o método **Finish** decodificará as propriedades do fluxo TNEF e as grava novamente na mensagem à que pertencem. 
  
Após a **chamada Concluir,** o ponteiro para o fluxo de encapsulamento aponta para o final dos dados TNEF. Se o provedor ou o gateway precisar usar os dados de fluxo TNEF após a chamada **Concluir,** ele deverá redefinir o ponteiro de fluxo para o início dos dados de fluxo TNEF. 
  
A implementação do TNEF relata problemas de codificação de fluxo TNEF sem interromper o **processo de** Concluir. A [estrutura STnefProblemArray](stnefproblemarray.md) retornada no parâmetro  _lpProblem_ indica quais atributos TNEF ou propriedades MAPI, se algum, não puderam ser processados. O valor retornado no membro **scode** de uma das estruturas **STnefProblem** contidas em **STnefProblemArray** indica o problema específico. O provedor ou gateway pode trabalhar na suposição de que todas as propriedades ou atributos para os quais **Finish** não retorna um relatório de problemas foram processados com êxito. 
  
Se um provedor ou gateway não funcionar com matrizes de problemas, ele poderá passar NULL em  _lpProblem_; nesse caso, nenhuma matriz do problema será retornada. 
  
O valor retornado em  _lpProblem_ só será válido se a chamada retornar S_OK. Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na **estrutura STnefProblemArray.** Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamada ou gateway não deverá usar ou liberar a estrutura. Se não ocorrer nenhum erro na chamada, o provedor de chamada ou gateway deverá liberar a memória para **o STnefProblemArray** chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa o **método ITnef::Finish** para concluir o processamento do novo fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriedade canônica PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

