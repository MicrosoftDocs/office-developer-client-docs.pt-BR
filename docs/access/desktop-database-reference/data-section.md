---
title: Seção Data (referência do banco de dados da área de trabalho do Access)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b8e3baf4d147edcc739e59933da4697c08cdef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295041"
---
# <a name="data-section"></a><span data-ttu-id="83788-102">Seção de dados</span><span class="sxs-lookup"><span data-stu-id="83788-102">Data section</span></span>

<span data-ttu-id="83788-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83788-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83788-p101">A seção de dados define os dados do conjunto de linhas, juntamente com quaisquer atualizações, inserções ou exclusões pendentes. A seção de dados pode conter zero ou mais linhas. E pode conter apenas dados de um conjunto de linhas no qual a linha é definida pelo esquema. Além disso, como já foi dito, as colunas sem dados podem ser omitidas. Se um atributo ou subelemento for usado na seção de dados e essa construção não tiver sido definida na seção de esquema, ela será ignorada silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="83788-p101">The data section defines the data of the rowset along with any pending updates, insertions, or deletions. The data section may contain zero or more rows. It may only contain data from one rowset where the row is defined by the schema. Also, as noted before, columns without any data may be omitted. If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="83788-109">String</span><span class="sxs-lookup"><span data-stu-id="83788-109">String</span></span>

<span data-ttu-id="83788-p102">Os caracteres XML reservados em dados de texto devem ser substituídos por entidades de caracteres adequadas. Por exemplo, no nome de empresa "Joe's Garage", o caractere de aspa simples deve ser substituído por uma entidade. A linha real teria esta aparência:</span><span class="sxs-lookup"><span data-stu-id="83788-p102">Reserved XML characters in text data must be replaced with appropriate character entities. For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity. The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="83788-113">Os seguintes caracteres são reservados em XML e devem ser substituídos por entidades de caractere: {',",&, \< } \> .</span><span class="sxs-lookup"><span data-stu-id="83788-113">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="83788-114">Binária</span><span class="sxs-lookup"><span data-stu-id="83788-114">Binary</span></span>

<span data-ttu-id="83788-115">Dados binários são codificados em bin.hex (ou seja, um byte mapeia para dois caracteres, um caractere por nibble).</span><span class="sxs-lookup"><span data-stu-id="83788-115">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="83788-116">DateTime</span><span class="sxs-lookup"><span data-stu-id="83788-116">DateTime</span></span>

<span data-ttu-id="83788-117">O formato variant VT DATE não é diretamente suportado XML-Data \_ tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="83788-117">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="83788-118">O formato correto para datas com um componente de data e hora é aaaa-mm-dd **T** hh:mm:ss.</span><span class="sxs-lookup"><span data-stu-id="83788-118">The correct format for dates with both a data and time component is yyyy-mm-dd **T** hh:mm:ss.</span></span>

<span data-ttu-id="83788-119">Para obter mais informações sobre formatos de data especificados por XML, consulte [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="83788-119">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="83788-120">Quando a especificação XML-Data define dois tipos de dados equivalentes (por exemplo, i4 == int), o ADO grava o nome amigável, mas lê ambos.</span><span class="sxs-lookup"><span data-stu-id="83788-120">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="83788-121">Gerenciando alterações pendentes</span><span class="sxs-lookup"><span data-stu-id="83788-121">Managing pending changes</span></span>

<span data-ttu-id="83788-p104">Um **Recordset** pode ser aberto no modo de atualização imediata ou em lotes. Quando aberto no modo de atualização em lotes com cursores do cliente, todas as alterações feitas no **Recordset** ficam em um estado pendente, até que o método **UpdateBatch** seja chamado. As alterações pendentes também persistem quando o **Recordset** é salvo. Em XML, elas são representadas pelo uso dos elementos "update" definidos em urn:schemas-microsoft-com:rowset. Além disso, se um conjunto de linhas puder ser atualizado, a propriedade atualizável deverá ser definida como verdadeira na definição da linha. Por exemplo, para definir que a tabela Shippers contém alterações pendentes, a definição de linha teria esta aparência:</span><span class="sxs-lookup"><span data-stu-id="83788-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="83788-128">Isso instrui o Persistence Provider para exibir os dados para que o ADO possa construir um objeto **Recordset** atualizável.</span><span class="sxs-lookup"><span data-stu-id="83788-128">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="83788-129">Os dados de exemplo a seguir mostram a aparência das inserções, alterações e exclusões no arquivo persistente:</span><span class="sxs-lookup"><span data-stu-id="83788-129">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

```xml 
<rs:data> 
  <z:row ShipperID="2" CompanyName="United Package"  
    Phone="(503) 555-3199"/> 
<rs:update> 
  <rs:original> 
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/> 
  </rs:original> 
  <z:row Phone="(503) 552-7134"/> 
</rs:update> 
<rs:insert> 
  <z:row ShipperID="12" CompanyName="Lightning Shipping"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="13" CompanyName="Thunder Overnight"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="14" CompanyName="Blue Angel Air Delivery"  
    Phone="(505) 111-2222"/> 
</rs:insert> 
<rs:delete> 
  <z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/> 
</rs:delete> 
</rs:data> 
```

<span data-ttu-id="83788-p105">Uma atualização sempre contém a linha de dados original inteira, seguida pelos dados da linha alterada. A linha alterada pode conter todas as colunas ou apenas aquelas que realmente foram alteradas. No exemplo anterior, a linha de Shipper 2 não é alterada, enquanto apenas a coluna Phone teve os valores de Shipper 3 alterados e, portanto, é a única coluna incluída na linha alterada. As linhas inseridas para Shippers 12, 13 e 14 são consideradas juntas em lote em uma marca rs:insert. Observe que as linhas excluídas também podem ser consideradas juntas em lote, embora isso não seja mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="83788-p105">An update always contains the entire original row data followed by the changed row data. The changed row may contain all of the columns or only those columns that have actually changed. In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row. The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag. Note that deleted rows may also be batched together, although this is not shown above.</span></span>

