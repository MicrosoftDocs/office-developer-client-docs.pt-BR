---
title: Propriedade ActiveConnection (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 2d2ed71f938089d3238eddee91f0c533bba266c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880005"
---
# <a name="activeconnection-property-ado-md"></a>Propriedade ActiveConnection (ADO MD)

**Aplica-se a**: Access 2013, o Office 2013

Indica a que objeto [Connection](connection-object-ado.md) do ADO pertence o conjunto de células ou o catálogo atual.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um objeto **Variant** que contém uma cadeia de caracteres que define uma conexão ou um objeto **Connection**. O padrão é vazio.

## <a name="remarks"></a>Comentários

Você pode definir esta propriedade como um objeto **Connection** válido do ADO ou como um cadeia de caracteres de conexão válida. Quando essa propriedade é definida como uma cadeia de caracteres de conexão, o provedor cria um novo objeto **Connection** usando essa definição e abre a conexão.

Se você usar o argumento **ActiveConnection** do método [Open](open-method-ado-md.md) para abrir um objeto [Cellset](cellset-object-ado-md.md), a propriedade **ActiveConnection** herdará o valor do argumento.

A definição da propriedade **ActiveConnection** de um objeto [Catalog](catalog-object-ado-md.md) como **Nothing** libera os dados associados, incluindo os dados da coleção [CubeDefs](cubedefs-collection-ado-md.md) e os objetos [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) e [Member](member-object-ado-md.md) relacionados. O fechamento do objeto **Connection** usado para abrir um **Catalog** tem o mesmo efeito que a definição da propriedade **ActiveConnection** como **Nothing**.

A alteração do banco de dados padrão da conexão referenciada pela propriedade **ActiveConnection** de um objeto **Catalog** invalida o conteúdo do **Catalog**.

Ocorrerá um erro se você tentar alterar a propriedade **ActiveConnection** de um objeto **Cellset** aberto.

> [!NOTE]
> [!OBSERVAçãO] No Visual Basic, lembre-se de usar a palavra-chave **Set** ao definir a propriedade **ActiveConnection** como um objeto **Connection**. Se você omitir a palavra-chave **Set**, estará realmente definindo a propriedade **ActiveConnection** de forma equivalente à propriedade padrão do objeto **Connection**, **ConnectionString**. O código funcionará; contudo, você criará uma conexão adicional à fonte de dados, que poderá ter implicações de desempenho negativas.

Ao usar o provedor de dados MSOLAP, defina a fonte de dados em uma cadeia de caracteres de conexão como o nome de um servidor e defina o catálogo inicial como o nome de um catálogo da fonte de dados. Para se conectar a um arquivo de cubo que esteja desconectado de um servidor, defina o local como o caminho completo para o arquivo .CUB. Nesse caso, defina o provedor com o respectivo nome. Por exemplo, a cadeia de caracteres a seguir conecta-se a um catálogo chamado Bobs Video Store em um servidor chamado Servername com o Provedor MSOLAP:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

A sequência a seguir conecta a um arquivo de cubo local no local c:\\MSDASDK\\amostras\\oledb\\olap\\dados\\bobsvid.cub:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

