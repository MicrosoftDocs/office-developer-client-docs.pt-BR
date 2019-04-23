---
title: Namespaces (referência do banco de dados de área de trabalho do Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288622"
---
# <a name="namespaces"></a><span data-ttu-id="63d32-102">Namespaces</span><span class="sxs-lookup"><span data-stu-id="63d32-102">Namespaces</span></span>

<span data-ttu-id="63d32-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63d32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63d32-104">O formato de persistência do XML no ADO usa estes espaços de nome.</span><span class="sxs-lookup"><span data-stu-id="63d32-104">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63d32-105">Prefixo</span><span class="sxs-lookup"><span data-stu-id="63d32-105">Prefix</span></span></p></th>
<th><p><span data-ttu-id="63d32-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="63d32-106">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63d32-107">s</span><span class="sxs-lookup"><span data-stu-id="63d32-107">s</span></span></p></td>
<td><p><span data-ttu-id="63d32-108">Refere-se &quot;ao namespace XML&quot; -data contendo os elementos e atributos que definem o esquema do <strong>Recordset</strong>atual.</span><span class="sxs-lookup"><span data-stu-id="63d32-108">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63d32-109">obrigatória</span><span class="sxs-lookup"><span data-stu-id="63d32-109">dt</span></span></p></td>
<td><p><span data-ttu-id="63d32-110">Refere-se à especificação das definições do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="63d32-110">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63d32-111">RS</span><span class="sxs-lookup"><span data-stu-id="63d32-111">rs</span></span></p></td>
<td><p><span data-ttu-id="63d32-112">Refere-se ao namespace que contém os elementos e os atributos específicos das propriedades e dos atributos do <strong>Recordset</strong> do ADO.</span><span class="sxs-lookup"><span data-stu-id="63d32-112">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63d32-113">z</span><span class="sxs-lookup"><span data-stu-id="63d32-113">z</span></span></p></td>
<td><p><span data-ttu-id="63d32-114">Refere-se ao esquema do conjunto de linhas atual.</span><span class="sxs-lookup"><span data-stu-id="63d32-114">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="63d32-p101">Um cliente não deve adicionar suas próprias marcas a esses espaços de nome, conforme definido pela especificação. Por exemplo, um cliente não deve definir um namespace como "urn:schemas-microsoft-com:rowset" e gravar algo como "rs:MyOwnTag." Para saber mais sobre os espaços de nome, consulte [Espaços de nome XML](https://www.w3.org/tr/xml-names/).</span><span class="sxs-lookup"><span data-stu-id="63d32-p101">A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>

> [!NOTE]
> <span data-ttu-id="63d32-118">[!OBSERVAçãO] O código da marca do esquema deve ser "RowsetSchema" e o namespace usado para fazer referência ao esquema do conjunto de linhas atual deve apontar para "#RowsetSchema".</span><span class="sxs-lookup"><span data-stu-id="63d32-118">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span>

<span data-ttu-id="63d32-119">Observe que o prefixo do namespace, aquela parte à direita dos dois-pontos e à esquerda do sinal de igual, é arbitrário.</span><span class="sxs-lookup"><span data-stu-id="63d32-119">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="63d32-p102">O usuário pode defini-lo como qualquer nome, contanto que esse nome seja usado de forma consistente no documento XML inteiro. O ADO sempre grava "s", "rs", "dt" e "z", mas esses nomes de prefixo não estão embutidos em código no componente de carga.</span><span class="sxs-lookup"><span data-stu-id="63d32-p102">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>



