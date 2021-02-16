---
title: Pastas de recebimento MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b22b8641d55037d3755fc9ae32b97455223bbd12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431936"
---
# <a name="mapi-receive-folders"></a>Pastas de Recebimento MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma pasta de recebimento contém mensagens de entrada de uma classe de mensagem específica. Associações de pastas de recebimento podem ser estabelecidas por clientes, pelo provedor de armazenamento de mensagens ou por MAPI. MAPI has two default receive folders: the root folder of the message store, and the Inbox folder of the interpersonal message (IPM) subtree. A pasta raiz do armazenamento de mensagens é a pasta de recebimento padrão para todas as mensagens de comunicação entre processos (IPC).
  
 A pasta Caixa de Entrada é criada pelo MAPI para cada novo armazenamento de mensagens e atua como a pasta de recebimento padrão para as seguintes classes de mensagem: 
  
- A classe de mensagens do IPM.
    
- A classe de mensagem de relatório.
    
- Uma classe vazia ou ausente.
    
Todas as mensagens de relatório, mesmo aquelas enviadas em resposta a uma mensagem IPC, são colocadas na pasta Caixa de Entrada. Os aplicativos cliente IPC que processam seus próprios relatórios devem adicionar explicitamente uma pasta de recebimento para a classe específica de relatório. Por exemplo, se um cliente espera receber mensagens com a IPC de classe. Paper.Order, ele deve chamar o método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para estabelecer uma pasta de recebimento para relatórios com a classe Report.IPC.Paper.Order. 
  
As associações de pastas de recebimento são baseadas na organização hierárquica das classes de mensagens. Os clientes podem estabelecer explicitamente uma associação entre uma pasta de recebimento e uma classe de mensagem ou usar as pastas de recebimento padrão MAPI. Normalmente, os clientes designam uma pasta para receber mensagens para uma classe base e todas as suas subclasses. Por exemplo, um cliente típico estabeleceria uma associação para mensagens com a classe **MyClass**. Em seguida, se o cliente recebeu mensagens com classes **MyClass.Home** ou **MyClass.Home.Kitchen.Computer**, essas mensagens devem ir para a pasta de recebimento para a classe base, **MyClass**.
  
Há três métodos de armazenamento de mensagens que os clientes usam para trabalhar com pastas de recebimento:
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
A tabela de pastas de recebimento é uma listagem de informações sobre todas as pastas de recebimento estabelecidas para um armazenamento de mensagens. O conjunto de colunas necessário inclui a classe de mensagem, a chave de registro e o identificador de entrada.
  
Para recuperar uma pasta de recebimento para uma classe de mensagem específica, os clientes passam a cadeia de caracteres de classe de mensagem para o [método IMsgStore::GetReceiveFolder.](imsgstore-getreceivefolder.md) O provedor de armazenamento de mensagens retorna um identificador de entrada para a pasta correspondente. Para implementar **GetReceiveFolder**, um provedor de armazenamento de mensagens deve usar um algoritmo que seleciona a pasta cuja classe de mensagem associada corresponde ao prefixo mais longo possível da classe de mensagem especificada. Por exemplo, suponha que o armazenamento de mensagens tenha as seguintes associações entre as pastas de recebimento e as classes de mensagens em sua tabela de pastas de recebimento:
  
- **As mensagens IPM** são colocadas na pasta Caixa de Entrada. 
    
- **IPM. Note.Sample** messages are placed in the Samples folder. 
    
A tabela a seguir mostra como as mensagens com várias classes seriam roteadas para a pasta de recebimento apropriada.
  
|**Classe de mensagem de entrada**|**Pasta de recebimento**|
|:-----|:-----|
|**IPM. Note.Sample.Simple** <br/> |Pasta De exemplos  <br/> |
|**IPM. Observação** <br/> |Pasta Caixa de Entrada  <br/> |
|**IPM. Cartão de ponto** <br/> |Pasta Caixa de Entrada  <br/> |
|**IPM. Note.Sample.Simple.Totally** <br/> |Pasta De exemplos  <br/> |
   
Os clientes chamam **o método SetReceiveFolder** para fazer uma associação explícita entre uma classe de mensagem específica e a pasta de recebimento. Quando uma mensagem é entregue a uma classe de mensagem vazia, MAPI coloca a mensagem na pasta de recebimento definida para um prefixo da classe vazia. Por exemplo, se seu cliente tiver uma pasta de recebimento estabelecida para mensagens com **IPM** de classe e uma mensagem com **IPM de classe. Note.Test** for delivered, this message will be placed in the receive folder for the **IPM** message class. 
  
Ao chamar **SetReceiveFolder**, os clientes normalmente passam uma cadeia de caracteres de classe de mensagem e o identificador de entrada da nova pasta de recebimento. No entanto, os clientes podem passar NULL para um ou ambos os parâmetros. A tabela a seguir descreve o comportamento que resulta da especificação de NULL para os parâmetros de classe de mensagem e identificador de entrada. 
  
|**_Parâmetro SetReceiveFolder_**|**Comportamento resultante**|
|:-----|:-----|
|Identificador de entrada definido como NULL  <br/> |O armazenamento de mensagens exclui a associação entre a classe de mensagens especificada e sua pasta de recebimento existente. Uma nova pasta de recebimento não é estabelecida.  <br/> Chamadas subsequentes **para GetReceiveFolder** com essa classe de mensagem retornarão a pasta de recebimento para um prefixo da classe de mensagem; para novos armazenamentos de mensagens, **GetReceiveFolder** retornará a Caixa de Entrada na subárvore do IPM.  <br/> |
|Classe de mensagem definida como NULL  <br/> |O armazenamento de mensagens altera a associação da classe de mensagem vazia para a pasta indicada. As mensagens de entrada cuja classe não é desconhecizada irão para essa pasta.  <br/> |
|Identificador de entrada e classe de mensagem definida como NULL  <br/> |O armazenamento de mensagens exclui a associação de classe/pasta para a classe de mensagem vazia. Você não deve definir os dois parâmetros como NULL, pois isso normalmente resulta em mensagens de entrada sendo colocadas na pasta raiz do armazenamento de mensagens, uma pasta invisível para o cliente.  <br/> |
   
Embora a classe de uma mensagem nunca deva estar vazia, uma classe de mensagem vazia pode ocorrer. É responsabilidade do armazenamento de mensagens atribuir a classe de mensagem ao **IPM** para novas mensagens de saída que tenham uma classe vazia; é responsabilidade do provedor de transporte atribuir **o IPM. Observe** como a classe para mensagens de entrada que têm qualquer classe vazia. 
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

