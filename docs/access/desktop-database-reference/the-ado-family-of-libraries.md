---
title: Família de bibliotecas do ADO
TOCTitle: The ADO Family of Libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9de96854eb08ff73fe9f70edf35dee972fd1a31e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462629"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="31fbc-102">Família de bibliotecas do ADO</span><span class="sxs-lookup"><span data-stu-id="31fbc-102">The ADO Family of Libraries</span></span>


<span data-ttu-id="31fbc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="31fbc-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="31fbc-104">Três bibliotecas principais compõem a família ADO: ADO (incluindo RDS), ADO MD e ADOX.</span><span class="sxs-lookup"><span data-stu-id="31fbc-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="31fbc-105">ADO</span><span class="sxs-lookup"><span data-stu-id="31fbc-105">ADO</span></span>

<span data-ttu-id="31fbc-p101">O ADO permite que os aplicativos clientes acessem e manipulem dados de um servidor de banco de dados através de um provedor OLE DB. Os principais benefícios do ADO são a facilidade de uso, a alta velocidade, baixa sobrecarga de memória e uma pequena superfície do disco. O ADO oferece suporte para os principais recursos de criação de aplicativos cliente/servidor e baseados na Web.</span><span class="sxs-lookup"><span data-stu-id="31fbc-p101">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider. The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint. ADO supports key features for building client/server and Web-based applications.</span></span>

<span data-ttu-id="31fbc-109">O ADO também apresenta o RDS (serviço de dados remoto), através do qual é possível mover dados de um servidor para um aplicativo cliente ou uma página da Web, manipular os dados no cliente e retornar atualizações para o servidor, em uma única viagem de ida e volta.</span><span class="sxs-lookup"><span data-stu-id="31fbc-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="31fbc-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="31fbc-110">ADO MD</span></span>

<span data-ttu-id="31fbc-p102">O Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) fornece acesso fácil aos dados multidimensionais de linguagens como Microsoft Visual Basic, Microsoft Visual C++ e Microsoft Visual J++. O ADO MD estende o ADO para incluir objetos específicos para dados multidimensionais, como os objetos **CubeDef** e **Cellset**. Com o ADO MD, é possível procurar esquema multidimensional, consultar um cubo e recuperar os resultados.</span><span class="sxs-lookup"><span data-stu-id="31fbc-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="31fbc-p103">Assim como o ADO, o ADO MD usa um provedor OLE DB subjacente para obter acesso aos dados. Para trabalhar com o ADO MD, o provedor deve ser um MDP (provedor de dados multidimensionais), conforme definido pela especificação do OLE DB para OLAP. Os MDPs apresentam os dados em modos de exibição multidimensionais, ao contrário dos TDPs (provedores de dados tabulares) que apresentam os dados em modos de exibição tabulares. Consulte a documentação do provedor OLE DB para OLAP para obter informações mais detalhadas sobre a sintaxe específica e os comportamentos que têm o suporte do provedor.</span><span class="sxs-lookup"><span data-stu-id="31fbc-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="31fbc-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="31fbc-118">ADOX</span></span>

<span data-ttu-id="31fbc-p104">O ADOX (Extensões do Microsoft ActiveX Data Objects para linguagem de definição de dados e segurança) é uma extensão do modelo de objetos e programação do ADO. O ADOX inclui objetos para criação e modificação de esquema, bem como para segurança. Por ser uma abordagem da manipulação de esquema baseada em objeto, é possível escrever código que funcionará em várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.</span><span class="sxs-lookup"><span data-stu-id="31fbc-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="31fbc-p105">O ADOX é uma biblioteca associada aos objetos básicos do ADO. Ele expõe objetos adicionais para criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, inclui objetos de segurança para manter os usuários e grupos e para conceder e revogar permissões nos objetos.</span><span class="sxs-lookup"><span data-stu-id="31fbc-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

