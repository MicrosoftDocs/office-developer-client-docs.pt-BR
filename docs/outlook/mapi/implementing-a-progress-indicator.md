---
title: Implementar um indicador de progresso
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
# <a name="implementing-a-progress-indicator"></a>Implementar um indicador de progresso

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas das operações iniciadas pelos clientes levam muito tempo. Um dos parâmetros de entrada para essas operações possivelmente demoradas é um ponteiro para um objeto Progress — um objeto que implementa a interface [método imapiprogress: IUnknown](imapiprogressiunknown.md) . Os objetos Progress controlam a aparência e a exibição de indicadores de progresso e são implementados por clientes e por MAPI. Você pode escolher se deseja ou não implementar um objeto Progress. A implementação de MAPI estará disponível para provedores de serviços usarem se você optar por não fornecer uma implementação. 
  
Os objetos Progress funcionam com as seguintes partes de dados:
  
- Um valor global mínimo que, quando o método [método imapiprogress::P rogress](imapiprogress-progress.md) é chamado, deve ser menor ou igual ao valor do parâmetro _ulValue_ . No início da operação, _ulValue_ será igual a esse valor mínimo. 
    
- Um valor global máximo que, quando o método **método imapiprogress::P rogress** é chamado, deve ser maior ou igual ao parâmetro _ulValue_ . No final da operação, _ulValue_ será igual a esse valor máximo. 
    
- Um valor sinalizador que indica se o andamento corresponde a um item de nível superior ou inferior.
    
- Um valor que indica o nível atual de progresso para a operação.
    
- O número de itens processados atualmente em relação ao total.
    
- O número total de itens a serem processados durante a operação.
    
Os valores mínimo e máximo representam o início e o fim da operação em formato numérico. Use 1 para o valor mínimo inicial e 1000 para o valor máximo inicial, passando estes valores para provedores de serviços nos métodos [método imapiprogress:: GetMin](imapiprogress-getmin.md) e [método imapiprogress:: GetMax](imapiprogress-getmax.md) . Os provedores de serviços redefinem esses valores quando chamam [método imapiprogress::](imapiprogress-setlimits.md)setlimits. 
  
O valor flags é usado pelos provedores de serviços para determinar como eles devem definir os outros valores. Inicialize o valor de sinalizadores para MAPI_TOP_LEVEL e retorne esse valor em sua **** implementação de GetFlags até que o provedor de serviços o redefina chamando setlimits. **** 
  
Na sua implementação do método **** setlimits, salve as cópias locais de cada um dos parâmetros: _lpulMin_, _lpulMax_e _lpulFlags_. Esses valores devem estar prontamente disponíveis quando um provedor de serviços chama seus métodos **GetMin**, **GetMax**ou GetFlags. **** 
  
Para atualizar a exibição do indicador de progresso, os provedores de serviços chamam o método **método imapiprogress::P rogress** . Há três parâmetros para este método: um valor, uma contagem e um total. Use o primeiro parâmetro, _ulValue_, para exibir o indicador de progresso. O parâmetro _ulValue_ é o indicador de progresso e será igual ao global _ulMin_ somente no início da operação e igual ao global _ulMax_ somente na conclusão da operação. 
  
Use o segundo e terceiro parâmetros, _ulCount_ e _ulTotal_, se disponível, para exibir uma mensagem opcional, como "5 itens concluídos de 10". Se o segundo e terceiro parâmetros estiverem definidos como 0, você poderá escolher se o indicador de andamento deve ou não ser alterado visualmente. Alguns provedores de serviços definem esses parâmetros como zeros para indicar que estão processando um subobjeto cujo progresso é monitorado em relação a um objeto pai. Nessa situação, faz sentido alterar a exibição somente quando o objeto pai relata o progresso. Alguns provedores de serviços passam por zeros nesses parâmetros a cada vez. 
  

