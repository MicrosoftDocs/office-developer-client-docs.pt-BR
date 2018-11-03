---
title: Seção de dados (referência de banco de dados da área de trabalho do Access)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98215394af89df30a95fcb9c5a757368cb64d4f1
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946374"
---
# <a name="data-section"></a>Seção de dados

**Aplica-se a**: Access 2013, o Office 2013

A seção de dados define os dados do conjunto de linhas, juntamente com quaisquer atualizações, inserções ou exclusões pendentes. A seção de dados pode conter zero ou mais linhas. E pode conter apenas dados de um conjunto de linhas no qual a linha é definida pelo esquema. Além disso, como já foi dito, as colunas sem dados podem ser omitidas. Se um atributo ou subelemento for usado na seção de dados e essa construção não tiver sido definida na seção de esquema, ela será ignorada silenciosamente.

## <a name="string"></a>Sequência de caracteres

Os caracteres XML reservados em dados de texto devem ser substituídos por entidades de caracteres adequadas. Por exemplo, no nome de empresa "Joe's Garage", o caractere de aspa simples deve ser substituído por uma entidade. A linha real teria esta aparência:

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

Os seguintes caracteres são reservados em XML e devem ser substituídos por entidades de caracteres: {', ", &,\<,\>}.

## <a name="binary"></a>Binário

Dados binários são codificados em bin.hex (ou seja, um byte mapeia para dois caracteres, um caractere por nibble).

## <a name="datetime"></a>DateTime

A variante VT\_formato de data não é suportado diretamente pelos tipos de dados de dados XML. O formato correto datas com uma data e a hora de componente é aaaa-mm-dd**T**hh.

Para obter mais informações sobre formatos de data especificados por XML, consulte [W3C Xmldatahttp nota](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).

Quando a especificação XML-Data define dois tipos de dados equivalentes (por exemplo, i4 == int), o ADO grava o nome amigável, mas lê ambos.

## <a name="managing-pending-changes"></a>Gerenciando alterações pendentes

Um **Recordset** pode ser aberto no modo de atualização imediata ou em lotes. Quando aberto no modo de atualização em lotes com cursores do cliente, todas as alterações feitas no **Recordset** ficam em um estado pendente, até que o método **UpdateBatch** seja chamado. As alterações pendentes também persistem quando o **Recordset** é salvo. Em XML, elas são representadas pelo uso dos elementos "update" definidos em urn:schemas-microsoft-com:rowset. Além disso, se um conjunto de linhas puder ser atualizado, a propriedade atualizável deverá ser definida como verdadeira na definição da linha. Por exemplo, para definir que a tabela Shippers contém alterações pendentes, a definição de linha teria esta aparência:

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

Isso instrui o Persistence Provider para exibir os dados para que o ADO possa construir um objeto **Recordset** atualizável.

Os dados de exemplo a seguir mostram a aparência das inserções, alterações e exclusões no arquivo persistente:

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

Uma atualização sempre contém a linha de dados original inteira, seguida pelos dados da linha alterada. A linha alterada pode conter todas as colunas ou apenas aquelas que realmente foram alteradas. No exemplo anterior, a linha de Shipper 2 não é alterada, enquanto apenas a coluna Phone teve os valores de Shipper 3 alterados e, portanto, é a única coluna incluída na linha alterada. As linhas inseridas para Shippers 12, 13 e 14 são consideradas juntas em lote em uma marca rs:insert. Observe que as linhas excluídas também podem ser consideradas juntas em lote, embora isso não seja mostrado acima.

