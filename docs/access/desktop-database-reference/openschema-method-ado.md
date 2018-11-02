---
title: Método OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 846d1c0f73ba4a17f166fffc7c1bb4682ad31d49
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921163"
---
# <a name="openschema-method-ado"></a>Método OpenSchema (ADO)


**Aplica-se a**: Access 2013, o Office 2013


Obtém informações do esquema do banco de dados a partir doprovedor .

## <a name="syntax"></a>Sintaxe

**Definir * * * recordset* = *conexão*. OpenSchema (* QueryType * *critérios*, *SchemaID*)

## <a name="return-values"></a>Valor de retorno

Retorna um objeto [Recordset](recordset-object-ado.md) que contém informações de esquema. O **Recordset** será aberto como um cursorestático somente de leitura. O *QueryType* determina quais colunas aparecem no **Recordset**.

## <a name="parameters"></a>Parâmetros

  - *QueryType*

  - Qualquer valor [SchemaEnum](schemaenum.md) que represente o tipo de consulta de esquema a ser executado.

  - *Criteria*

  - Opcional. Uma matriz de restrições de consulta para cada opção *QueryType* , conforme listado em **SchemaEnum**.

  - *SchemaID*

  - O GUID de uma consulta de esquema do provedor não definida pela especificação de banco de dados OLE. Este parâmetro é obrigatório se *QueryType* estiver definida como **adSchemaProviderSpecific**; Caso contrário, ele não é usado.

## <a name="remarks"></a>Comentários

O método **OpenSchema** retorna informações auto-descritivas sobre a fonte de dados, tais como quais tabelas estão na fonte de dados, as colunas nas tabelas e os tipos de dados suportados.

O argumento *QueryType* é um GUID que indica as colunas (esquemas) é retornado. A especificação de banco de dados OLE tem uma lista completa de esquemas.

O argumento *Criteria* limita os resultados de uma consulta de esquema. *Criteria* especifica uma matriz de valores que devem ocorrer em um subconjunto de colunas correspondentes, denominadas *colunas de restrição*, no **Recordset** resultante.

A constante **adSchemaProviderSpecific** é usado para o argumento *QueryType* se o provedor define suas próprias consultas de esquema não padrão fora dos listados acima. Quando esta constante é usado, o argumento *SchemaID* é necessária para passar o GUID do esquema de consulta para executar. Se *QueryType* estiver definido como **adSchemaProviderSpecific** , mas *SchemaID* não for fornecido, ocorrerá um erro.

Os provedores não precisam suportar todas as consultas de esquema padrão do banco de dados OLE. Especificamente, apenas **adSchemaTables**, **adSchemaColumns** e **adSchemaProviderTypes** são necessárias pela especificação do banco de dados OLE. No entanto, o provedor não é necessário para suportar as restrições de *critérios* listadas acima para essas consultas de esquema.

**Uso de serviço de dados remotos** O método **OpenSchema** não está disponível em um objeto de [Conexão](connection-object-ado.md) do cliente.


> [!NOTE]
> <P>No Visual Basic, as colunas que têm um inteiro sem sinal de quatro bytes (DBTYPE UI4) no <STRONG>Recordset</STRONG> retornado do método <STRONG>OpenSchema</STRONG> no objeto <STRONG>Connection</STRONG> não podem ser comparadas a outras variáveis. Para obter mais informações sobre os tipos de dados de banco de dados OLE, consulte o Capítulo 13 e o Apêndice A do <EM>Microsoft OLE DB Programmer's Reference</EM>.</P>


