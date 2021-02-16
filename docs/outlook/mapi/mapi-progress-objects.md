---
title: Objetos de progresso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422023"
---
# <a name="mapi-progress-objects"></a>Objetos de progresso MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Com os métodos e dados de um objeto de progresso, você pode controlar como o indicador relata o progresso. Embora um cliente ou MAPI implemente o objeto de progresso, a maior parte da carga de garantir a correção da exibição do progresso se enquadra nos provedores de serviços. Você pode garantir sua precisão especificando uma ordem e um valor específicos para os parâmetros que são passados para métodos de objeto de progresso.
  
Os parâmetros a seguir são passados para objetos de progresso:
  
- Uma bitmask de sinalizadores, definida com [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) e recuperada com [IMAPIProgress::GetFlags](imapiprogress-getflags.md).
    
- Um valor mínimo (local e global), definido com **SetLimits** e recuperado com [IMAPIProgress::GetMin](imapiprogress-getmin.md).
    
- Um valor máximo (local e global), definido com **SetLimits** e recuperado com [IMAPIProgress::GetMax](imapiprogress-getmax.md).
    
- Um valor que indica a porcentagem atual de conclusão da operação, passada para [IMAPIProgress::P ess](imapiprogress-progress.md).
    
- Uma contagem do número de objetos que foram processados até agora, passada para **Progress**.
    
- Uma contagem do número total de objetos envolvidos na operação, passada para **Progress**.
    
Todos os provedores de serviços iniciam seu processamento de exibição de progresso com uma chamada para **IMAPIProgress::GetFlags** para recuperar a configuração de sinalizadores presentes. Atualmente, os sinalizadores só podem ser definidos como MAPI_TOP_LEVEL. Os clientes e o MAPI inicializam o sinalizador para MAPI_TOP_LEVEL, confiando nos provedores de serviços para des limpa-lo quando apropriado. 
  
O valor de sinalizadores é definido como MAPI_TOP_LEVEL enquanto você estiver trabalhando com o objeto de nível superior na operação. O objeto de nível superior é o objeto que é chamado pelo cliente para iniciar uma operação. Em uma operação de cópia de pasta, esta é a pasta que está sendo copiada. Em uma operação de exclusão de pasta, essa é a pasta que está sendo excluída. Ao fazer uma chamada para processar um objeto de nível inferior ou subobjeto, limpe o valor de sinalizadores. Em uma operação de cópia de pasta, os subobjetos são as subpastas que estão na pasta que está sendo copiada. 
  
MAPI allows you to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress, so causing the indicator display to proceed smoothly in a single positive direction. A definição MAPI_TOP_LEVEL sinalizador de MAPI_TOP_LEVEL afetará as configurações dos outros parâmetros em chamadas subsequentes para o objeto de progresso. 
  
Como pode ser nãotrivial definir valores de parâmetro apropriados para uma exibição de progresso em todos os níveis de uma operação de vários níveis, alguns provedores de serviços optam por não mostrar o progresso de subobjetos. 
  
 **Para evitar mostrar o progresso de subobjetos**
  
- Passe NULL para  _o parâmetro lpProgress_ na chamada para processar um subobjeto. Por exemplo, se você estiver copiando pastas, essa será a chamada para o método [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) de uma subpasta. 
    
- Escreva um código especial para determinar como interpretar o _parâmetro lpProgress._ Como um valor NULL para o parâmetro  _lpProgress_ também pode significar que o cliente deve exibir o progresso usando a implementação de MAPI, um código especial é necessário para determinar quando ignorar o parâmetro  _lpProgress_ e quando chamar [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Chame **IMAPIProgress::SetLimits** para definir ou limpar o sinalizador MAPI_TOP_LEVEL e definir valores mínimo e máximo locais e globais. O valor da configuração de sinalizadores afeta se o objeto de progresso entende os valores mínimo e máximo para serem locais ou globais. Quando o MAPI_TOP_LEVEL sinalizador é definido, esses valores são considerados globais e usados para calcular o progresso de toda a operação. Os objetos de progresso inicializam o valor mínimo global como 0 e o valor máximo global como 1000. 
  
Quando MAPI_TOP_LEVEL não estiver definido, os valores mínimo e máximo serão considerados locais e usados internamente pelos provedores para exibir o progresso de subobjetos de nível inferior. Os objetos de progresso salvam os valores mínimo e máximo local apenas para que possam ser retornados aos provedores quando **GetMin** e **GetMax** são chamados. 
  
O valor, a contagem de objetos e os parâmetros totais do objeto são de entrada para o **método IMAPIProgress::P ess.** O parâmetro value, um número que indica a porcentagem de progresso, é obrigatório. Se o MAPI_TOP_LEVEL sinalizador estiver definido, você também poderá passar uma contagem de objetos e um total de objetos. Alguns clientes usam esses valores para exibir uma frase como "5 itens concluídos em 10" com o indicador de progresso. O progresso de uma operação pode ser relatado estritamente como uma porcentagem ou como uma porcentagem e em termos do número de itens que foram processados fora do total a ser processado. Por exemplo, se você for um provedor de armazenamento de mensagens e estiver executando uma operação de cópia que está copiando 10 pastas, o indicador de progresso poderá fornecer ao usuário informações adicionais exibindo uma frase como "1 de 10", "2 de 10", "3 de 10" e assim por diante até que a operação seja concluída. 
  
## <a name="see-also"></a>Confira também



[Indicadores de progresso MAPI](mapi-progress-indicators.md)

