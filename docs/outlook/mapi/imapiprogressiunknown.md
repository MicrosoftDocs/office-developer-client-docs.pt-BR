---
title: Método imapiprogress IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270074"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementa um objeto Progress que fornece aplicativos cliente com um indicador de progresso. Um indicador de progresso é uma exibição da interface do usuário que mostra a porcentagem de conclusão de uma operação, como copiar pastas entre repositórios de mensagens. Os aplicativos de cliente e MAPI implementam objetos Progress e provedores de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos de progresso  <br/> |
|Implementado por:  <br/> |Aplicativos de MAPI e cliente  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProgress  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Atualiza o indicador de progresso com uma exibição do progresso conforme ele é feito na conclusão da operação.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Retorna as configurações de sinalizador do objeto Progress para o nível de operação em que as informações de progresso são calculadas.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Retorna o número máximo de itens na operação para o qual as informações de progresso são exibidas.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Retorna o valor mínimo no método [](imapiprogress-setlimits.md) setlimits para o qual as informações de progresso são exibidas.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Define os limites inferior e superior para o número de itens na operação e os sinalizadores que controlam como as informações de progresso são calculadas para a operação.  <br/> |
   
## <a name="remarks"></a>Comentários

MAPI inclui um parâmetro _lpProgress_ em muitos dos métodos que executam operações potencialmente demoradas.  _lpProgress_ aponta para uma implementação de cliente de um objeto Progress. Os clientes que implementam a interface **método imapiprogress** definem esse parâmetro para apontar para sua implementação; Os clientes que não implementam **método imapiprogress** definem o parâmetro como NULL. Para exibir um indicador de progresso durante o processamento da operação, os provedores de serviços usam o objeto Progress fornecido pelo cliente, se disponível ou uma implementação MAPI (indicada quando _lpProgress_ está definido como nulo). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Files**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MapiProgress. h e MapiProgress. cpp  <br/> |Não aplicável  <br/> |Se a configuração método imapiprogress estiver habilitada, o MFCMAPI passará uma implementação do **método imapiprogress** para todas as funções que MFCMAPI invocas que aceitam uma implementação.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

