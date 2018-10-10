---
title: 'Apêndice A: provedores'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbd9536edd15f923af85f2fadad8b696077af4a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464489"
---
# <a name="appendix-a-providers"></a>Apêndice A: provedores


**Aplica-se a**: Access 2013 | Office 2013


Esta seção descreve três tipos de provedores: provedores de dados, provedores de serviços e componentes de serviço. Os provedores enquadram-se em duas categorias: os que fornecem dados e os que fornecem serviços. Um *provedor de dados* possui seus próprios dados e os exibe em um formulário tabular para seu aplicativo. Um *provedor de serviços* encapsula um serviço gerando e consumindo dados, aumentando recursos em aplicativos do ADO. Um provedor de serviços também pode ser definido posteriormente como um *componente de serviço*, que deverá trabalhar juntamente com outros provedores ou componentes de serviços.

## <a name="data-providers"></a>Provedores de dados

O ADO é poderoso e flexível, pois pode conectar-se a qualquer um dos vários provedores de dados e ainda apresentar o mesmo modelo de programação, independentemente dos recursos específicos de um determinado provedor.

Entretanto, pelo fato de cada provedor de dados ser exclusivo, a forma de seu aplicativo interagir com o ADO variará ligeiramente de acordo com o provedor de dados. As diferenças geralmente enquadram-se em três categorias:

  - Parâmetros de conexão na propriedade [ConnectionString](connectionstring-property-ado.md).

  - Uso do objeto [Command](command-object-ado.md).

  - Comportamento específico do provedor [Recordset](recordset-object-ado.md).

Os detalhes de cada um dos provedores de dados atualmente disponíveis na Microsoft estão relacionados a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Área</p></th>
<th><p>Tópico</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bancos de dados ODBC</p></td>
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Serviço de Indexação da Microsoft</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></p></td>
</tr>
<tr class="odd">
<td><p>Serviço do Active Directory da Microsoft</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></p></td>
</tr>
<tr class="even">
<td><p>Bancos de dados do Microsoft Jet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">OLE DB Provider for Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Bancos de dados Oracle</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Publicação na Internet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Propriedades dinâmicas específicas para o provedor

A coleção [Properties](properties-collection-ado.md) dos objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) e [Recordset](recordset-object-ado.md) incluem propriedades dinâmicasespecíficas para o provedor. Essas propriedades fornecem informações sobre a funcionalidade específica do provedor, além das propriedades internas que têm suporte do ADO.

Depois de estabelecer a conexão e criar esses objetos, utilize o método [Refresh](refresh-method-ado.md) na coleção **Properties** do objeto para obter as propriedades específicas para o provedor. Consulte a documentação do provedor e a Referência do programador do OLE DB para obter informações detalhadas sobre essas propriedades dinâmicas.

## <a name="service-providers"></a>Provedores de serviços

Para utilizar um provedor de serviços, você deverá fornecer uma palavra-chave. Também deverá conhecer as propriedades dinâmicas específicas para o provedor associadas a cada provedor de serviços. Os detalhes específicos para provedor são relacionados para cada um dos provedores de serviços atualmente disponíveis na Microsoft:

  - [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

  - [Microsoft OLE DB Persistence Provider](microsoft-ole-db-persistence-provider-ado-service-provider.md)

  - [Microsoft OLE DB Remoting Provider](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Componentes de serviço

O componente de serviço [Cursor Service para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) complementa as funções de suporte do cursor dos provedores de dados. Também exige uma palavra-chave e tem propriedades dinâmicas.

Para obter mais informações sobre provedores, consulte a documentação do Microsoft OLE DB no Microsoft Data Access Components SDK ou visite o site [Centro do Desenvolverdo da Plataforma de Dados](https://msdn.microsoft.com/data/default.aspx).

## <a name="provider-commands"></a>Comandos do provedor

Para cada provedor listado aqui, se seus aplicativos permitir que os usuários insiram as instruções SQL que os comandos do provedor, você deve sempre validar a entrada do usuário e ser cuidadoso de phishing possíveis usando a instrução SQL potencialmente perigosa, como, como parte do entrada do usuário.

