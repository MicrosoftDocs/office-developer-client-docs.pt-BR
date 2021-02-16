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
  
Lembre-se de que seu servidor de formulário é um aplicativo Win32. Dessa forma, há algumas tarefas relacionadas ao carregamento do servidor de formulário na memória e ao sair corretamente. Como todos os aplicativos do Windows, o ponto de entrada para seu servidor de formulário é a **função WinMain.** Esta função é o local apropriado para executar as seguintes tarefas: 
  
- Criar e registrar uma classe de janela para que o servidor de formulário possa interagir com outros componentes OLE.
    
- Criando e registrando uma classe de janela ou classes para as interfaces de usuário dos objetos de formulário.
    
- Chamando a [função MAPIInitialize.](mapiinitialize.md) **MAPIInitialize** também lida com a inicialização OLE necessária para você. Isso deve ser feito uma vez por instância do seu servidor de formulário. 
    
- Registrando um atom global com uma representação de cadeia de caracteres do identificador de classe do servidor de formulário (CLSID). Esse atom deve existir durante o tempo de vida do servidor de formulário.
    
- Chamar a função OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) para registrar a fábrica de classe do servidor de formulário com OLE. 
    
- Criar uma janela principal para receber mensagens. Essa janela provavelmente não precisa estar visível porque o usuário interagirá com as janelas específicas associadas a objetos de formulário individuais. No entanto, durante o desenvolvimento, a janela principal pode ser um local conveniente para depurar a saída ou o controle do servidor de formulário.
    
- Criar um loop de mensagem que é executado durante o tempo de vida do servidor de formulário, traduzindo e expedindo mensagens do Windows para objetos de formulário ativos.
    
Quando o servidor de formulário é final, ele deve executar as seguintes tarefas:
  
- Chame a função OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revogar o registro OLE da classe de mensagem. 
    
- Chame **MAPIUninitialize** para fechar corretamente a conexão do servidor de formulário com MAPI. 
    
- Exclua o atom global que contém a representação de cadeia de caracteres do identificador de classe.
    
## <a name="see-also"></a>Confira também



[Escrevendo código do servidor de formulário](writing-form-server-code.md)

