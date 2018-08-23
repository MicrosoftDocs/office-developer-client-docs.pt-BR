---
title: Implementar um indicador de progresso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1a359ec413da91b3e2819978e80ea0a921f6b245
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587121"
---
# <a name="implementing-a-progress-indicator"></a>Implementar um indicador de progresso

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas das operações iniciadas pelos clientes levar um período de tempo significativo. Um dos parâmetros de entrada para essas operações potencialmente demoradas é um ponteiro para um objeto de progresso — um objeto que implementa o [IMAPIProgress: IUnknown](imapiprogressiunknown.md) interface. Os objetos de progresso controlam a aparência e a exibição de indicadores de progresso e são implementados pelos clientes e por MAPI. Você pode escolher se deseja ou não implementar um objeto de andamento. A implementação do MAPI está disponível para provedores de serviço a ser usado se você optar por não fornecer uma implementação. 
  
Objetos de progresso trabalham com as seguintes partes dos dados:
  
- Um valor mínimo global que, quando o método [IMAPIProgress::Progress](imapiprogress-progress.md) é chamado, deve ser menor ou igual ao valor do parâmetro _ulValue_ . No início da operação, _ulValue_ será igual a este valor mínimo. 
    
- Um valor máximo global que, quando o método **IMAPIProgress::Progress** é chamado, deve ser maior ou igual ao parâmetro _ulValue_ . No final da operação, _ulValue_ será igual a esse valor máximo. 
    
- Sinalizadores de um valor que indica se o progresso corresponde a um parte superior ou diminuir nível de item.
    
- Um valor que indica o nível de progresso da operação atual.
    
- O número de itens atualmente processados em relação ao total.
    
- O número total de itens a serem processados durante a operação.
    
Os valores máximo e mínimo representam o início e término da operação no formulário numérico. Use 1 para o valor mínimo inicial e 1000 para o valor máximo inicial, passando esses valores com provedores de serviços nos métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) e [IMAPIProgress::GetMax](imapiprogress-getmax.md) . Provedores de serviços redefinir esses valores quando ele liga [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). 
  
O valor flags é usado pelos provedores de serviços para determinar como eles devem definir os outros valores. Inicializar o valor de sinalizadores para MAPI_TOP_LEVEL e retornar esse valor na sua implementação de **GetFlags** até que o provedor de serviços redefine chamando **SetLimits**. 
  
Em sua implementação do método **SetLimits** , salvar cópias locais de cada um dos parâmetros: _lpulMin_, _lpulMax_e _lpulFlags_. Esses valores devem ser prontamente disponíveis quando um provedor de serviço chama seus métodos **GetMin**, **GetMax**ou **GetFlags** . 
  
Para atualizar a exibição do indicador de progresso, provedores de serviços chamarem seu método de **IMAPIProgress::Progress** . Há três parâmetros para esse método: um valor, uma contagem e um total. Use o primeiro parâmetro, _ulValue_, para exibir o indicador de progresso. O parâmetro _ulValue_ é o indicador de progresso e será igual a global _ulMin_ somente no início da operação e igual a global _ulMax_ apenas na conclusão da operação. 
  
Use o segundo e terceiro parâmetros, _ulCount_ e _ulTotal_, se disponível, para exibir uma mensagem opcional, como "5 itens concluída fora de 10." Se o segundo e terceiro parâmetros forem definido como 0, você poderá escolher se deseja ou não alterar visualmente o indicador de progresso. Alguns provedores de serviços definido esses parâmetros como zeros para indicar que eles são processando um Subobjeto cujo andamento é monitorado em relação um objeto pai. Nessa situação, faz sentido para alterar a exibição somente quando o objeto pai relata o progresso. Alguns provedores de serviços passam zeros para esses parâmetros de cada vez. 
  

