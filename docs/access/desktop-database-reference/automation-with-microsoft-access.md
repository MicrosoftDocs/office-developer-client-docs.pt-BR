---
title: Automação com o Microsoft Access
TOCTitle: Automation with Microsoft Access
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bd0e230d2b4c31d497e913e8e1ccf4d2172402e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463980"
---
# <a name="automation-with-microsoft-access"></a>Automação com o Microsoft Access


**Aplica-se a**: Access 2013 | Office 2013

O Microsoft Access é um componente COM que oferece suporte à Automação, anteriormente denominada Automação OLE. O Microsoft Access oferece suporte à Automação de duas maneiras. A partir do Microsoft Access, você pode trabalhar com objetos fornecidos por um outro componente. O Microsoft Access também fornece seus objetos a outros componentes COM.

Você pode usar a palavra-chave **New** ou o método **CreateObject** para criar uma nova instância de um componente. Use o método **GetObject** para atribuir uma variável a uma instância de um componente.

No Microsoft Access, você pode definir uma referência à biblioteca de tipos de um componente para melhorar o desempenho quando você trabalha com aquele componente através da Automação. O Microsoft Access também inclui o Pesquisador de objeto, uma ferramenta que permite que você veja objetos na biblioteca de tipos de um outro componente, bem como seus métodos e propriedades.

A biblioteca de tipos do Microsoft Access fornece informações sobre os objetos do Microsoft Access aos outros componentes. Você pode [definir uma referência](https://msdn.microsoft.com/library/ff194944\(v=office.15\)) para o Microsoft Access digite biblioteca a partir de um componente e visualizar seus objetos no Pesquisador de objetos.

Para trabalhar com os objetos do Microsoft Access por meio da Automação, crie uma instância do objeto **[Application](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** do Microsoft Access. Por exemplo, suponha que você deseja exibir dados do Microsoft Excel em um formulário ou relatório do Microsoft Access. Para iniciar o Microsoft Access a partir do Microsoft Excel, use a palavra-chave **New** para criar uma instância do objeto **Application** do Microsoft Access. Também é possível usar o método **CreateObject** para criar uma nova instância do objeto **Application** do Microsoft Access ou usar o método **GetObject** para apontar uma variável de objeto para uma instância existente do Microsoft Access. Verifique a documentação do componente para determinar a qual sintaxe é oferecido suporte.

Assim que uma instância do Microsoft Access tiver sido iniciada, se você quiser controlar algum objeto do Microsoft Access, abra um banco de dados ou projeto (.adp) na janela do Microsoft Access usando o método **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))**, ou **[NewCurrentDatabase](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** para um banco de dados ou usando o método **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))**, ou **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** para um projeto.

Se você tiver aberto o Microsoft Access somente como um meio para usar os Objetos de Acesso a Dados fornecidos pelo Microsoft DAO, não será necessário abrir um banco de dados na janela do Microsoft Access. Use a propriedade **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** do objeto **Application** do Microsoft Access para acessar os objetos na biblioteca de objetos da Biblioteca de Objetos do Mecanismo do Banco de Dados do Microsoft Office 12.0 durante uma operação de Automação.

