---
título: automação com o Microsoft Access TOCTitle: automação com o Microsoft Access <<<<<<< ms:assetid cabeça: 39fde349-3ba3-7c7a-3c92-316641dc8712 ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15) ms:contentKeyID: ms.date 48544258: 18/09/2015 === Descrição: o Microsoft Access é um componente COM que oferece suporte a automação, anteriormente denominada automação OLE.
MS:AssetID: 39fde349-3ba3-7c7a-3c92-316641dc8712 ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15) ms:contentKeyID: ms.date 48544258: 10/16/2018
>>>>>>> mtps_version mestre: v=office.15 f1_keywords:
- vbaac10.chm13783 f1_categories:
- Office.Version=v15
---

# <a name="automation-with-microsoft-access"></a>Automação com o Microsoft Access

<<<<<<< Cabeça

=======
>>>>>>> **aplica-se**de mestre: Access 2013 | Office 2013

O Microsoft Access é um componente COM que oferece suporte à Automação, anteriormente denominada Automação OLE. O Microsoft Access oferece suporte à Automação de duas maneiras. A partir do Microsoft Access, você pode trabalhar com objetos fornecidos por um outro componente. O Microsoft Access também fornece seus objetos a outros componentes COM.

Você pode usar a palavra-chave **New** ou o método **CreateObject** para criar uma nova instância de um componente. Use o método **GetObject** para atribuir uma variável a uma instância de um componente.

No Microsoft Access, você pode definir uma referência à biblioteca de tipos de um componente para melhorar o desempenho quando você trabalha com aquele componente através da Automação. O Microsoft Access também inclui o Pesquisador de objeto, uma ferramenta que permite que você veja objetos na biblioteca de tipos de um outro componente, bem como seus métodos e propriedades.

<<<<<<< Biblioteca de tipos de cabeça o Microsoft Access fornece informações sobre os objetos do Microsoft Access para outros componentes. Você pode [definir uma referência](https://msdn.microsoft.com/library/ff194944\(v=office.15\)) para o Microsoft Access digite biblioteca a partir de um componente e visualizar seus objetos no Pesquisador de objetos.

Para trabalhar com os objetos do Microsoft Access por meio da Automação, crie uma instância do objeto **[Application](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** do Microsoft Access. Por exemplo, suponha que você deseja exibir dados do Microsoft Excel em um formulário ou relatório do Microsoft Access. Para iniciar o Microsoft Access a partir do Microsoft Excel, use a palavra-chave **New** para criar uma instância do objeto **Application** do Microsoft Access. Também é possível usar o método **CreateObject** para criar uma nova instância do objeto **Application** do Microsoft Access ou usar o método **GetObject** para apontar uma variável de objeto para uma instância existente do Microsoft Access. Verifique a documentação do componente para determinar a qual sintaxe é oferecido suporte.

Assim que uma instância do Microsoft Access tiver sido iniciada, se você quiser controlar algum objeto do Microsoft Access, abra um banco de dados ou projeto (.adp) na janela do Microsoft Access usando o método **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))**, ou **[NewCurrentDatabase](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** para um banco de dados ou usando o método **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))**, ou **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** para um projeto.

Se você tiver aberto o Microsoft Access somente como um meio para usar os Objetos de Acesso a Dados fornecidos pelo Microsoft DAO, não será necessário abrir um banco de dados na janela do Microsoft Access. Use a propriedade **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** do objeto **Application** do Microsoft Access para acessar os objetos na biblioteca de objetos da Biblioteca de Objetos do Mecanismo do Banco de Dados do Microsoft Office 12.0 durante uma operação de Automação.
=======
A biblioteca de tipos do Microsoft Access fornece informações sobre os objetos do Microsoft Access aos outros componentes. Você pode [definir uma referência](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) para o Microsoft Access digite biblioteca a partir de um componente e visualizar seus objetos no Pesquisador de objetos.

Para trabalhar com os objetos do Microsoft Access por meio da Automação, crie uma instância do objeto **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** do Microsoft Access. Por exemplo, suponha que você deseja exibir dados do Microsoft Excel em um formulário ou relatório do Microsoft Access. Para iniciar o Microsoft Access a partir do Microsoft Excel, use a palavra-chave **New** para criar uma instância do objeto **Application** do Microsoft Access. Também é possível usar o método **CreateObject** para criar uma nova instância do objeto **Application** do Microsoft Access ou usar o método **GetObject** para apontar uma variável de objeto para uma instância existente do Microsoft Access. Verifique a documentação do componente para determinar a qual sintaxe é oferecido suporte.

Depois de você ter iniciado uma instância do Microsoft Access, se você quiser controlar quaisquer objetos do Microsoft Access, você deve abrir um banco de dados ou projeto (. adp) na janela do Microsoft Access usando o **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** ou o **[NewCurrentDatabase ](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** método para um banco de dados ou usando o **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** ou o método **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** para um projeto.

Se você abriu o Microsoft Access somente como um meio de usando o Data Access Objects fornecidos pelo Microsoft DAO, você não precisará abrir um banco de dados na janela do Microsoft Access. Você pode usar a propriedade **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** do objeto de **aplicativo** do Microsoft Access para acessar objetos na biblioteca do Microsoft Office 12.0 Access banco de dados de mecanismo de objeto durante uma operação de automação.
>>>>>>> mestre

