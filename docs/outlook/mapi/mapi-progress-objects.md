---
title: Objetos Progress de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340072"
---
# <a name="mapi-progress-objects"></a>Objetos Progress de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Com os métodos e os dados de um objeto Progress, você pode controlar como o indicador relata o progresso. Embora um cliente ou MAPI implemente o objeto Progress, a maior parte do fardo de garantir a exatidão da exibição do progresso ocorre nos provedores de serviço. Você pode garantir a precisão especificando um determinado pedido e valor para os parâmetros passados para os métodos de objeto Progress.
  
Os seguintes parâmetros são passados para objetos Progress:
  
- Uma bitmask de sinalizadores, definida com [método imapiprogress::](imapiprogress-setlimits.md) setlimits e recuperado com [método imapiprogress:: GetFlags](imapiprogress-getflags.md).
    
- Um valor mínimo (local e global), definido com **** setlimits e recuperado com [método imapiprogress:: GetMin](imapiprogress-getmin.md).
    
- Um valor máximo (local e global), definido com **** setlimits e recuperado com [método imapiprogress:: GetMax](imapiprogress-getmax.md).
    
- Um valor que indica a porcentagem atual de conclusão da operação, passada para [método imapiprogress::P rogress](imapiprogress-progress.md).
    
- Uma contagem do número de objetos que foram processados até o momento, passados para o **andamento**.
    
- Uma contagem do número total de objetos envolvidos na operação, passados para **Progress**.
    
Todos os provedores de serviços começam seu processamento de exibição de progresso com uma chamada para **método imapiprogress:: GetFlags** para recuperar a configuração de sinalizadores atuais. No momento, os sinalizadores podem ser definidos somente como MAPI_TOP_LEVEL. Os clientes e o MAPI inicializam o sinalizador para o MAPI_TOP_LEVEL, confiando nos provedores de serviços para limpá-lo quando apropriado. 
  
O valor flags é definido como MAPI_TOP_LEVEL enquanto você estiver trabalhando com o objeto de nível superior na operação. O objeto de nível superior é o objeto que é chamado pelo cliente para iniciar uma operação. Em uma operação de cópia de pasta, esta é a pasta que está sendo copiada. Em uma operação de exclusão de pasta, esta é a pasta que está sendo excluída. Quando você faz uma chamada para processar um objeto de nível inferior, ou subobjeto, limpe o valor flags. Em uma operação de cópia de pasta, os subobjetos são as subpastas que estão na pasta que está sendo copiada. 
  
O MAPI permite que você diferencie objetos de nível superior e subobjetos com o sinalizador MAPI_TOP_LEVEL para que todos os objetos envolvidos em uma operação possam usar a mesma implementação do [método imapiprogress](imapiprogressiunknown.md) para mostrar o progresso, fazendo com que o indicador seja exibido para prosseguir sem problemas em uma única direção positiva. Se o sinalizador MAPI_TOP_LEVEL está ou não definido afeta as configurações dos outros parâmetros nas chamadas subsequentes para o objeto Progress. 
  
Como pode ser não trivial definir valores de parâmetros apropriados para uma exibição de progresso em todos os níveis de uma operação de vários níveis, alguns provedores de serviços elegem não mostrar o progresso dos subobjetos. 
  
 **Para evitar a exibição do progresso de subobjetos**
  
- Passe NULL para o parâmetro _lpProgress_ na chamada para processar um subobjeto. Por exemplo, se você estiver copiando pastas, esta é a chamada para o método [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) da subpasta. 
    
- Escreva código especial para determinar como interpretar o parâmetro _lpProgress_ . Como um valor nulo para o parâmetro _lpProgress_ também pode significar que o cliente deve exibir o progresso usando a implementação MAPI, o código especial é necessário para determinar quando ignorar o parâmetro _lpProgress_ e quando chamar [ IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Chame **método imapiprogress::** setlimits para definir ou limpar o sinalizador MAPI_TOP_LEVEL e para definir os valores globais e mínimos locais e máximos. O valor da configuração sinalizadores afeta se o objeto Progress entenderá os valores mínimo e máximo como local ou global. Quando o sinalizador MAPI_TOP_LEVEL é definido, esses valores são considerados globais e são usados para calcular o progresso de toda a operação. Os objetos Progress inicializam o valor global mínimo como 0 e o valor global máximo como 1000. 
  
Quando MAPI_TOP_LEVEL não estiver definido, os valores mínimo e máximo serão considerados locais e serão usados internamente por provedores para exibir o progresso de subobjetos de nível inferior. Os objetos Progress salvam os valores mínimo e máximo locais apenas para que eles possam ser retornados aos provedores quando **GetMin** e **GetMax** são chamados. 
  
O valor, a contagem de objetos e o total de parâmetros de objeto são entrada para o método **método imapiprogress::P rogress** . O parâmetro value, um número que indica a porcentagem de progresso, é necessário. Se o sinalizador MAPI_TOP_LEVEL estiver definido, você também pode passar uma contagem de objeto e um total de objeto. Alguns clientes usam esses valores para exibir uma frase como "5 itens concluídos de 10" com o indicador de progresso. O andamento em uma operação pode ser relatado estritamente como uma porcentagem ou como uma porcentagem e em termos do número de itens que foram processados fora do total a ser processado. Por exemplo, se você é um provedor de armazenamento de mensagens e está executando uma operação de cópia que está copiando 10 pastas, o indicador de progresso pode fornecer ao usuário informações adicionais exibindo uma frase como "1 de 10", "2 de 10", "3 de 10" e assim por diante até que a operação seja concluída. 
  
## <a name="see-also"></a>Confira também



[Indicadores de progresso MAPI](mapi-progress-indicators.md)

