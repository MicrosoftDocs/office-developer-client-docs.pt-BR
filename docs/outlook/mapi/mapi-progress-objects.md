---
title: Objetos de progresso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c6079a62464231536c0fa6b5bacc291997fe38d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567920"
---
# <a name="mapi-progress-objects"></a>Objetos de progresso MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Com os métodos e os dados de um objeto de andamento, você pode controlar como os relatórios no indicador de progresso. Embora um cliente ou MAPI implementa o objeto de andamento, a maioria da responsabilidade de garantir a exatidão da exibição de progresso cai em provedores de serviços. Você pode garantir a precisão especificando uma ordem específica e um valor para os parâmetros que são passados para os métodos do objeto de progresso.
  
Os seguintes parâmetros são passados para os objetos de andamento:
  
- Uma bitmask dos sinalizadores, definido com [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) e recuperadas com [IMAPIProgress::GetFlags](imapiprogress-getflags.md).
    
- Um valor mínimo (global e local), definidas com **SetLimits** e recuperadas com [IMAPIProgress::GetMin](imapiprogress-getmin.md).
    
- Um valor máximo (global e local), definidas com **SetLimits** e recuperadas com [IMAPIProgress::GetMax](imapiprogress-getmax.md).
    
- Um valor que indica a porcentagem atual de conclusão da operação, passada para [IMAPIProgress::Progress](imapiprogress-progress.md).
    
- Uma contagem do número de objetos que até o momento foram processados, passadas para **o progresso**.
    
- Uma contagem do número total de objetos envolvidos na operação, passada para **o progresso**.
    
Todos os provedores de serviço começam sua exibição progresso processamento com uma chamada para **IMAPIProgress::GetFlags** para recuperar os sinalizadores presentes configuração. Atualmente, os sinalizadores podem ser definidos somente para MAPI_TOP_LEVEL. Clientes e MAPI inicializar o sinalizador para MAPI_TOP_LEVEL, a terceira em provedores de serviços para desmarcá-la quando apropriado. 
  
O valor de flags for definido como MAPI_TOP_LEVEL enquanto você estiver trabalhando com o objeto de nível superior na operação. O objeto de nível superior é o objeto que é chamado pelo cliente para iniciar uma operação. Em uma operação de cópia da pasta, essa é a pasta que está sendo copiada. Em uma operação de exclusão de pasta, essa é a pasta que está sendo excluída. Quando você faz uma chamada para o processo de um objeto de nível inferior ou subobjeto, desmarque o valor flags. Em uma operação de cópia da pasta, subobjetos são as subpastas que estão na pasta que está sendo copiada. 
  
MAPI permite diferenciar entre objetos de nível superior e subobjetos com o sinalizador MAPI_TOP_LEVEL para que todos os objetos envolvidos em uma operação podem usar a mesma implementação [IMAPIProgress](imapiprogressiunknown.md) para mostrar o progresso, causando assim a exibição de indicador para Continue suavemente em uma única direção positiva. Ou não o sinalizador MAPI_TOP_LEVEL é definido afeta as configurações dos outros parâmetros em chamadas subsequentes ao objeto de andamento. 
  
Como ele pode ser não trivial para definir valores de parâmetro apropriado para uma exibição de progresso em todos os níveis de uma operação de vários níveis, alguns provedores de serviços optar por não mostrar o progresso para subobjetos. 
  
 **Para evitar mostrando o andamento para subobjetos**
  
- Passe nulo para o parâmetro _lpProgress_ na chamada para processar um Subobjeto. Por exemplo, se você estiver copiando pastas, isso é a chamada ao método de [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) uma subpasta. 
    
- Escreva código especial para determinar como interpretar o parâmetro _lpProgress_ . Porque um valor nulo para o parâmetro _lpProgress_ também pode significar que o cliente deve exibir o progresso usando a implementação de MAPI, código especial é necessário para determinar quando ignorar o parâmetro _lpProgress_ e quando chamadas [ IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md).
    
Chame **IMAPIProgress::SetLimits** para definir ou limpar o sinalizador MAPI_TOP_LEVEL e para definir os valores máximo e mínimo de globais e locais. O valor dos sinalizadores afeta a definição se o objeto de progresso entende os valores mínimos e máximo para ser local ou global. Quando o sinalizador MAPI_TOP_LEVEL estiver definido, esses valores são considerados globais e são usados para calcular o progresso de toda a operação. Objetos de progresso inicializar o valor mínimo global como 0 e o valor máximo global a 1000. 
  
Quando MAPI_TOP_LEVEL não estiver definida, os valores mínimos e máximo são considerados locais e são usados internamente pelo provedores para exibir o progresso de subobjetos de nível inferiores. Objetos de progresso salvar os valores mínimos e máximo locais somente para que pode ser retornados para provedores quando **GetMin** e **GetMax** são chamados. 
  
O valor, contagem de objeto e parâmetros total de objetos são de entrada para o método **IMAPIProgress::Progress** . O parâmetro value, um número que indica a porcentagem de progresso, é necessário. Se o sinalizador MAPI_TOP_LEVEL estiver definido, você também pode passar uma contagem de objetos e um total de objeto. Alguns clientes usam esses valores para exibir uma frase como "5 itens concluída fora de 10" com o indicador de progresso. Progresso de uma operação pode ser informado estritamente como uma porcentagem, ou como uma porcentagem e em termos de número de itens que tenham sido processadas sem total a serem processados. Por exemplo, se você for um provedor de armazenamento de mensagem e você estiver executando uma operação de cópia que está copiando 10 pastas, o indicador de progresso pode fornecer o usuário com informações adicionais exibindo uma frase como "1 de 10", "2 de 10", "3 de 10" , e assim por diante, até que a operação seja concluída. 
  
## <a name="see-also"></a>Confira também



[Indicadores de progresso MAPI](mapi-progress-indicators.md)

