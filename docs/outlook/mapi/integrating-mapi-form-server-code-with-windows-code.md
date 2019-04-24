---
title: Integrando o código do servidor de formulário MAPI ao código do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332176"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integrando o código do servidor de formulário MAPI ao código do Windows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Lembre-se de que seu servidor de formulário é um aplicativo Win32. Assim, há algumas tarefas relacionadas ao carregamento do servidor de formulários na memória e de saída limpa. Como todos os aplicativos do Windows, o ponto de entrada para seu servidor de formulários é a função **WinMain** . Essa função é o local apropriado para executar as seguintes tarefas: 
  
- Criar e registrar uma classe de janela para que seu servidor de formulário possa interagir com outros componentes OLE.
    
- Criar e registrar uma classe de janela ou classes para as interfaces de usuário de seus objetos de formulário.
    
- Chamar a função [MAPIInitialize](mapiinitialize.md) . **MAPIInitialize** também trata a inicialização OLE necessária para você. Isso deve ser feito uma vez por instância do seu servidor de formulários. 
    
- Registro de um átomo global com uma representação de cadeia de caracteres do identificador de classe (CLSID) do servidor de formulário. Esse átomo deve existir durante o tempo de vida do servidor de formulário.
    
- Chamar a função OLE [](https://msdn.microsoft.com/library/ms693407.aspx) CoRegisterClassObject para registrar a fábrica de classes do seu servidor de formulário com OLE. 
    
- Criar uma janela principal para receber mensagens. Essa janela provavelmente não precisa estar visível porque o usuário será interagir com as janelas específicas associadas a objetos de formulário individuais. No enTanto, durante o desenvolvimento, a janela principal pode ser um local conveniente para a depuração de saída ou controle de seu servidor de formulários.
    
- Criação de um loop de mensagem que é executado durante o tempo de vida do servidor de formulário, tradução e expedição de mensagens do Windows para objetos de formulário ativos.
    
Quando o servidor de formulário é encerrado, ele deve executar as seguintes tarefas:
  
- Chame a função OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revogar o registro OLE da classe de mensagem. 
    
- Chame **MAPIUninitialize** para fechar corretamente a conexão do servidor de formulário com MAPI. 
    
- Exclua o átomo global que contém a representação de cadeia de caracteres do identificador de classe.
    
## <a name="see-also"></a>Confira também



[Gravando código de servidor de formulário](writing-form-server-code.md)

