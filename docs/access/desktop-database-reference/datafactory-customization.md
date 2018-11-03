---
title: Personalização de DataFactory
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9de748b85e4bf6076c37f49e9d9bc7ff3b0bfe62
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947565"
---
# <a name="datafactory-customization"></a><span data-ttu-id="b1fe0-102">Personalização de DataFactory</span><span class="sxs-lookup"><span data-stu-id="b1fe0-102">DataFactory customization</span></span>


<span data-ttu-id="b1fe0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1fe0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1fe0-p101">O RDS (Remote Data Service) oferece uma forma de acesso fácil aos dados em um sistema cliente/servidor de três camadas. Um controle de dados de cliente especifica os parâmetros da sequência de conexão e da sequência de comando para executar uma consulta em uma fonte de dados remota, ou parâmetros da sequência de conexão e do objeto [Recordset](recordset-object-ado.md) para executar uma atualização.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="b1fe0-p102">Os parâmetros são passados para um programa de servidor, que executa a operação de acesso a dados na fonte de dados remota. O RDS disponibiliza um programa de servidor padrão, o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md). O objeto **RDSServer.DataFactory** retorna qualquer objeto **Recordset** produzido por uma consulta ao cliente.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="b1fe0-p103">Entretanto, o **RDSServer.DataFactory** limita-se à realização de consultas e atualizações. Ele não pode executar qualquer validação ou processamento nas sequência de comando ou de conexão.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="b1fe0-p104">Com o ADO, você pode especificar o funcionamento de **DataFactory** em conjunto com outro tipo de programa de servidor, denominado *manipulador*. O manipulador pode modificar as sequências de comando e de conexão do cliente antes de elas serem usadas para acessar a fonte de dados. Ele também pode impor direitos de acesso, que permitem que o cliente leia e grave dados na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-p104">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*. The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="b1fe0-114">Os parâmetros usados pelo manipulador para modificar parâmetros de cliente e direitos de acesso são especificados nas seções de um arquivo de personalização.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="b1fe0-115">Consulte os tópicos a seguir para obter mais informações sobre como personalizar o objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="b1fe0-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="b1fe0-116">Noções básicas sobre o arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="b1fe0-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="b1fe0-117">Seção Connect do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="b1fe0-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="b1fe0-118">Seção SQL do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="b1fe0-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="b1fe0-119">Seção UserList do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="b1fe0-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="b1fe0-120">Seção de Logs do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="b1fe0-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="b1fe0-121">Configurações necessárias do cliente</span><span class="sxs-lookup"><span data-stu-id="b1fe0-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="b1fe0-122">Como escrever o seu próprio manipulador personalizado</span><span class="sxs-lookup"><span data-stu-id="b1fe0-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
