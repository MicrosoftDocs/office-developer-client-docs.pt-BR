---
title: Integrar o código do servidor de formulário MAPI ao código do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397860"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>Integrar o código do servidor de formulário MAPI ao código do Windows

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Lembre-se de que seu servidor de formulário é um aplicativo Win32. Assim, há algumas tarefas relacionadas ao carregar o seu servidor de formulário na memória e saindo corretamente. Como todos os aplicativos do Windows, o ponto de entrada para seu servidor de formulário é a função **WinMain** . Essa função é o local adequado para realizar as seguintes tarefas: 
  
- Criar e registrar uma classe de janela para que seu servidor de formulário possa interagir com outros componentes do OLE.
    
- Criar e registrar uma classe de janela ou classes para interfaces do usuário dos objetos do formulário.
    
- Chamar a função de [MAPIInitialize](mapiinitialize.md) . **MAPIInitialize** trata a OLE inicialização necessária para você, também. Isso deve ser feito uma vez por instância do seu servidor do formulário. 
    
- Registrando um atom global com uma representação de cadeia de caracteres de identificador do servidor formulário de classe (CLSID). Este atom deve existir para o tempo de vida do servidor do formulário.
    
- Chamar a função OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) para registrar o alocador de classe do seu servidor de formulário com OLE. 
    
- Criando uma janela principal para receber mensagens. Essa janela provavelmente não precisa estar visível porque o usuário interagirá com as janelas específicas associadas a objetos de formulário individuais. No entanto, durante o desenvolvimento, a janela principal pode ser um local conveniente para controle do seu servidor do formulário ou saída de depuração.
    
- Criando um loop de mensagem que é executado para o tempo de vida do servidor do formulário, traduzindo e expedir mensagens do windows para objetos do formulário ativo.
    
Quando seu servidor de formulário é encerrado, ele deve executar as seguintes tarefas:
  
- Chame a função OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revogar o registro do OLE da classe da mensagem. 
    
- Chame **MAPIUninitialize** para fechar corretamente a conexão do servidor de formulário para MAPI. 
    
- Exclua o atom global que contém a representação de cadeia de caracteres do identificador de classe.
    
## <a name="see-also"></a>Confira também



[Escrevendo códigos de servidor do formulário](writing-form-server-code.md)

