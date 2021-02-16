---
title: Implementando um indicador de progresso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6972c960705c336aa6ff96d81b48ccbd490a22ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435093"
---
# <a name="implementing-a-progress-indicator"></a>Implementando um indicador de progresso

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas das operações iniciadas pelos clientes levam um tempo significativo. Um dos parâmetros de entrada para essas operações potencialmente longas é um ponteiro para um objeto de progresso — um objeto que implementa a interface [IMAPIProgress : IUnknown.](imapiprogressiunknown.md) Os objetos de progresso controlam a aparência e a exibição dos indicadores de progresso e são implementados por clientes e por MAPI. Você pode escolher se implementará ou não um objeto de progresso. A implementação de MAPI está disponível para os provedores de serviços usarem se você optar por não fornecer uma implementação. 
  
Os objetos de progresso funcionam com as seguintes partes de dados:
  
- Um valor mínimo global que, quando seu método [IMAPIProgress::P ess](imapiprogress-progress.md) é chamado, deve ser menor ou igual ao valor do parâmetro _ulValue._ No início da operação,  _ulValue_ será igual a esse valor mínimo. 
    
- Um valor máximo global que, quando seu método **IMAPIProgress::P ess** é chamado, deve ser maior ou igual ao parâmetro _ulValue._ No final da operação,  _ulValue_ será igual a esse valor máximo. 
    
- Um valor de sinalizador que indica se o andamento corresponde a um item de nível superior ou inferior.
    
- Um valor que indica o nível atual de progresso da operação.
    
- O número de itens atualmente processados em relação ao total.
    
- O número total de itens a serem processados durante a operação.
    
Os valores mínimo e máximo representam o início e o fim da operação em formato numérico. Use 1 para o valor mínimo inicial e 1000 para o valor máximo inicial, passando esses valores para provedores de serviços nos métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) e [IMAPIProgress::GetMax.](imapiprogress-getmax.md) Os provedores de serviços redefinem esses valores quando chamam [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). 
  
O valor de sinalizadores é usado pelos provedores de serviços para determinar como eles devem definir os outros valores. Inicialize o valor de sinalizadores para MAPI_TOP_LEVEL e retorne esse valor em sua implementação de **GetFlags** até que o provedor de serviços o redefina chamando **SetLimits**. 
  
Em sua implementação do **método SetLimits,** salve cópias locais de cada um dos parâmetros:  _lpulMin_,  _lpulMax_ e  _lpulFlags_. Esses valores devem estar prontamente disponíveis quando um provedor de serviços chamar seus métodos **GetMin,** **GetMax** ou **GetFlags.** 
  
Para atualizar a exibição do indicador de progresso, os provedores de serviços chamam seu **método IMAPIProgress::P ress.** Há três parâmetros para esse método: um valor, uma contagem e um total. Use o primeiro parâmetro,  _ulValue,_ para exibir o indicador de progresso. O  _parâmetro ulValue_ é o indicador de progresso e será igual ao  _ulMin_ global apenas no início da operação e igual a  _ulMax_ global apenas na conclusão da operação. 
  
Use o segundo e o terceiro parâmetros,  _ulCount_ e  _ulTotal,_ se disponíveis, para exibir uma mensagem opcional, como "5 itens concluídos em 10". Se o segundo e o terceiro parâmetros são definidos como 0, você pode escolher se deve ou não alterar visualmente o indicador de progresso. Alguns provedores de serviços configuram esses parâmetros como zeros para indicar que estão processando um subobjeto cujo progresso é monitorado em relação a um objeto pai. Nessa situação, faz sentido alterar a exibição somente quando o objeto pai relata progresso. Alguns provedores de serviços sempre passam zeros para esses parâmetros. 
  

