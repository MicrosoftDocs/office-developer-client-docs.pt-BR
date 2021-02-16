---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419643"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementa um objeto de progresso que fornece aos aplicativos cliente um indicador de progresso. Um indicador de progresso é uma exibição de interface do usuário que mostra a porcentagem de conclusão de uma operação, como copiar pastas entre os armazenamentos de mensagens. MapI and client applications implement progress objects and service providers use them. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos de progresso  <br/> |
|Implementado por:  <br/> |MAPI e aplicativos cliente  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProgress  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Atualiza o indicador de progresso com uma exibição do progresso conforme ele é feito na direção da conclusão da operação.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Retorna configurações de sinalizador do objeto de progresso para o nível de operação no qual as informações de progresso são calculadas.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Retorna o número máximo de itens na operação para o qual as informações de progresso são exibidas.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Retorna o valor mínimo no [método SetLimits](imapiprogress-setlimits.md) para o qual as informações de progresso são exibidas.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Define os limites inferior e superior para o número de itens na operação e os sinalizadores que controlam como as informações de progresso são calculadas para a operação.  <br/> |
   
## <a name="remarks"></a>Comentários

MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.  _lpProgress_ aponta para uma implementação de cliente de um objeto de progresso. Os clientes que implementam a interface **IMAPIProgress** configuram esse parâmetro para apontar para sua implementação; os clientes que não implementam **IMAPIProgress configuram** o parâmetro como NULL. Para exibir um indicador de progresso durante o processamento da operação, os provedores de serviços usam o objeto de progresso fornecido pelo cliente, se disponível, ou uma implementação de MAPI (indicado quando  _lpProgress_ está definido como NULL). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Files**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MapiProgress.h e MapiProgress.cpp  <br/> |Não aplicável  <br/> |Se a configuração IMAPIProgress estiver habilitada, MFCMAPI passará uma implementação **IMAPIProgress** para todas as funções invocadas por MFCMAPI que aceitem uma implementação.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

