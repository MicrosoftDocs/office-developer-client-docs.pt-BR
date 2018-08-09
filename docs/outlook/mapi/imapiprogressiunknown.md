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
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767143"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Implementa um objeto de progresso que fornece aos aplicativos de cliente com um indicador de progresso. Um indicador de progresso é uma exibição da interface do usuário que mostra a porcentagem de conclusão de uma operação, como copiar pastas entre as lojas de mensagem. Aplicativos MAPI e cliente implementam objetos de progresso e provedores de serviços de usá-los. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de progresso  <br/> |
|Implementada por:  <br/> |Aplicativos MAPI e cliente  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIProgress  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Atualiza o indicador de progresso com uma exibição do progresso da conforme ele é feito rumo à conclusão da operação.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Retorna sinaliza as configurações do objeto de andamento para o nível de operação no qual as informações sobre o andamento é calculado.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Retorna o número máximo de itens na operação para o qual andamento informações são exibidas.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Retorna o valor mínimo no método [SetLimits](imapiprogress-setlimits.md) para qual andamento informações são exibidas.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Define os limites inferiores e superiores para o número de itens da operação e os sinalizadores que controlam como as informações sobre o andamento é calculada para a operação.  <br/> |
   
## <a name="remarks"></a>Comentários

MAPI inclui um parâmetro _lpProgress_ em muitos dos métodos que executam operações potencialmente demoradas.  _lpProgress_ aponta para uma implementação do cliente de um objeto de andamento. Clientes que implementam a interface **IMAPIProgress** defina esse parâmetro para apontar para sua implementação; clientes que não implementam **IMAPIProgress** defina o parâmetro como NULL. Para exibir um indicador de progresso durante o processamento da operação, provedores de serviços usam o objeto de progresso fornecido pelo cliente, se disponível, ou uma implementação de MAPI (indicada quando _lpProgress_ estiver definido como NULL). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivos**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MapiProgress.h e MapiProgress.cpp  <br/> |Não aplicável  <br/> |Se a configuração IMAPIProgress estiver habilitada, MFCMAPI passará uma implementação **IMAPIProgress** a todas as funções que invoca MFCMAPI que aceitam uma implementação.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

