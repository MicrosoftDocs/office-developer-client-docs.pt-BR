---
title: Usando o ADO for Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305898"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="aa0d3-102">Uso do ADO para Publicação de Internet</span><span class="sxs-lookup"><span data-stu-id="aa0d3-102">Using ADO for Internet publishing</span></span>


<span data-ttu-id="aa0d3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa0d3-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="aa0d3-104">[O OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) mostra um exemplo específico de acesso a dados heterogêneos com o ADO.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-104">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO.</span></span> <span data-ttu-id="aa0d3-105">Embora os exemplos desta seção sejam específicos para usar o Internet Publishing Provider, os princípios demonstrados devem ser semelhantes ao usar o ADO com outros provedores para dados heterogêneos, como um provedor para um armazenamento de email.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-105">While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an email store.</span></span>

## <a name="urls"></a><span data-ttu-id="aa0d3-106">URLs</span><span class="sxs-lookup"><span data-stu-id="aa0d3-106">URLs</span></span>

<span data-ttu-id="aa0d3-p102">As URLs podem ser usadas como uma alternativa para as sequências de conexão e o texto de comando a fim de especificar fontes de dados e o local de arquivos e diretórios. Você pode utilizá-las com os objetos [Connection](connection-object-ado.md) e **Recordset** existentes, e também com os objetos **Record** e **Stream**.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-p102">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories. You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="aa0d3-109">Para obter mais informações sobre como usar URLs, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="aa0d3-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="aa0d3-110">Campos de registro</span><span class="sxs-lookup"><span data-stu-id="aa0d3-110">Record Fields</span></span>

<span data-ttu-id="aa0d3-p103">A diferença entre dados heterogêneos e dados homogêneos é que para o primeiro, cada linha de dados, ou **Registro**, pode ter um conjunto diferente de colunas, ou **Campos**. No caso dos dados homogêneos, cada linha possui o mesmo conjunto de colunas. Para obter mais informações sobre os campos específicos do Internet Publishing Provider, consulte [Registros e campos extras fornecidos pelo provedor](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="aa0d3-p103">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="aa0d3-114">Acrescentando novos campos</span><span class="sxs-lookup"><span data-stu-id="aa0d3-114">Appending New Fields</span></span>

<span data-ttu-id="aa0d3-115">Vários objetos ADO foram aprimorados para funcionar junto com objetos **Record** e **Stream**.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="aa0d3-116">O método [Append](fields-collection-ado.md) da coleção [Fields](append-method-ado.md), que cria e adiciona um objeto [Field](field-object-ado.md) à coleção, também pode especificar o valor de **Field**.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="aa0d3-117">O método [Update](update-method-ado.md) finaliza a adição ou a exclusão de campos da coleção.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="aa0d3-118">Como atalho e alternativa ao método **Append**, você pode criar campos simplesmente atribuindo um valor a um campo indefinido ou excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="aa0d3-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa0d3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa0d3-119">See also</span></span>

- [<span data-ttu-id="aa0d3-120">Tópicos do Cenário de Publicação na Internet</span><span class="sxs-lookup"><span data-stu-id="aa0d3-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)
