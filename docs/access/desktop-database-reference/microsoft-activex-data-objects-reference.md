---
title: Referência do Microsoft ActiveX Data Objects
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31d314ebbdc43bd6e50c187cafcb68028d03a7e5
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996801"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="1cb39-102">Referência do Microsoft ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="1cb39-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="1cb39-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cb39-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="1cb39-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="1cb39-104">Purpose</span></span>

<span data-ttu-id="1cb39-105">O Microsoft ActiveX Data Objects (ADO) permite que aplicativos clientes acessem e manipulem dados em um servidor de banco de dados através de um provedor de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1cb39-105">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="1cb39-106">Suas principais vantagens são facilidade de uso, alta velocidade, pouca sobrecarga de memória e necessidade de pouco espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="1cb39-106">Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="1cb39-107">O ADO oferece suporte a recursos-chave para criar aplicativos baseados na web e cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="1cb39-107">ADO supports key features for building client/server and web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="1cb39-108">RDS</span><span class="sxs-lookup"><span data-stu-id="1cb39-108">RDS</span></span>

<span data-ttu-id="1cb39-109">ADO também recursos Remote Data Service (RDS), ao qual você pode mover dados de um servidor a um aplicativo cliente ou página da Web, manipular os dados no cliente e retornar as atualizações para o servidor em uma única viagem de ida e.</span><span class="sxs-lookup"><span data-stu-id="1cb39-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="1cb39-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="1cb39-110">ADO MD</span></span>

<span data-ttu-id="1cb39-p102">O Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) permite fácil acesso a dados multidimensionais em linguagens como Microsoft Visual Basic, Microsoft Visual C++ e Microsoft Visual J++. O ADO MD amplia o Microsoft ActiveX Data Objects (ADO) para incluir objetos específicos de dados multidimensionais, como objetos CubeDef e Cellset. Com o ADO MD, você pode procurar esquemas multidimensionais, consultar um cubo e recuperar os resultados.</span><span class="sxs-lookup"><span data-stu-id="1cb39-p102">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="1cb39-p103">Como o ADO, o ADO MD usa um provedor de OLE DB subjacente para obter acesso aos dados. Para utilizar o ADO MD, o provedor deve ser um MDP (provedor de dados multidimensionais), como definido na especificação do OLE DB para OLAP. Os MDPs apresentam dados em modos de exibição multidimensionais, ao contrário de TDPs (provedores de dados tabulares) que apresentam dados em modos de exibição tabulares. Consulte a documentação do provedor OLE DB para OLAP para obter informações mais detalhadas sobre a sintaxe e os comportamentos específicos aos quais seu provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="1cb39-p103">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="1cb39-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="1cb39-118">ADOX</span></span>

<span data-ttu-id="1cb39-p104">O Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) é uma extensão dos objetos do ADO e do modelo de programação. O ADOX contém objetos para a criação e modificação de esquemas, bem como para segurança. Como ele consiste em uma abordagem baseada em objetos para a manipulação de esquemas, você pode criar um código a ser utilizado com várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.</span><span class="sxs-lookup"><span data-stu-id="1cb39-p104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="1cb39-p105">O ADOX é uma biblioteca que acompanha os principais objetos do ADO. Ele apresenta objetos adicionais para a criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, contém objetos de segurança para manter usuários e grupos, bem como para conceder e revogar permissões em objetos.</span><span class="sxs-lookup"><span data-stu-id="1cb39-p105">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="1cb39-125">O ADO 2.5 componentes principais</span><span class="sxs-lookup"><span data-stu-id="1cb39-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="1cb39-126">[Guia do programador](ado-programmer-s-guide.md): uma introdução ao uso do ADO, RDS, ADO MD e ADOX.</span><span class="sxs-lookup"><span data-stu-id="1cb39-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="1cb39-127">[Referência do programador](ado-programmer-s-reference-topics.md): Esta seção da documentação do ADO contém tópicos para cada ADO, RDS, ADO MD e objeto ADOX, coleção, propriedade, propriedade dinâmica, método, evento e enumeração.</span><span class="sxs-lookup"><span data-stu-id="1cb39-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="1cb39-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cb39-128">Feedback</span></span>

<span data-ttu-id="1cb39-129">Você pode enviar comentários sobre a documentação ou os exemplos do ADO diretamente para e equipe de documentação do ADO.</span><span class="sxs-lookup"><span data-stu-id="1cb39-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

