---
title: Método OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288333"
---
# <a name="openschema-method-ado"></a>Método OpenSchema (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Obtém informações do esquema do banco de dados a partir doprovedor .

## <a name="syntax"></a>Sintaxe

**Set***recordset*  =  *connection*. OpenSchema (* QueryType*, *Criteria*, *SchemaID*)

## <a name="return-values"></a>Valor de retorno

Retorna um objeto [Recordset](recordset-object-ado.md) que contém informações de esquema. O **Recordset** será aberto como um cursorestático somente de leitura. O *QueryType* determina quais colunas aparecem no **Recordset**.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*QueryType* |Qualquer valor [SchemaEnum](schemaenum.md) que represente o tipo de consulta de esquema a ser executado.|
|*Criteria* |Opcional. Uma matriz de restrições de consulta para cada opção de *QueryType*, conforme listado em **SchemaEnum**.|
|*SchemaID* |O GUID de uma consulta de esquema do provedor não definida pela especificação de banco de dados OLE. Este parâmetro é obrigatório se *QueryType* estiver definido como **adSchemaProviderSpecific**; caso contrário, não será utilizado.|

## <a name="remarks"></a>Comentários

O método **OpenSchema** retorna informações auto-descritivas sobre a fonte de dados, tais como quais tabelas estão na fonte de dados, as colunas nas tabelas e os tipos de dados suportados.

O argumento *QueryType* é um GUID que indica as colunas (esquemas) retornadas. A especificação de banco de dados OLE tem uma lista completa de esquemas.

O argumento *Criteria* limita os resultados de uma consulta de esquema. *Criteria* especifica uma matriz de valores que devem ocorrer em um subconjunto de colunas correspondentes, denominadas *colunas de restrição*, no **Recordset** resultante.

A constante **adSchemaProviderSpecific** será utilizada para o argumento *QueryType* se o provedor definir suas próprias consultas de esquema não-padrão além das listadas acima. Quando essa constante é utilizada, o argumento *SchemaID* precisa passar o GUID da consulta de esquema para execução. Se *QueryType* for definido como **adSchemaProviderSpecific** mas *SchemaID* não for fornecido, ocorrerá um erro.

Os provedores não precisam suportar todas as consultas de esquema padrão do banco de dados OLE. Especificamente, apenas **adSchemaTables**, **adSchemaColumns** e **adSchemaProviderTypes** são necessárias pela especificação do banco de dados OLE. No entanto, o provedor não precisa suportar as restrições de *Criteria* listadas acima para essas consultas de esquema.

**Uso do Remote Data Service** O **método OpenSchema** não está disponível em um objeto [Connection do](connection-object-ado.md) lado do cliente.

> [!NOTE]
> No Visual Basic, as colunas que têm um inteiro sem sinal de quatro bytes (DBTYPE UI4) no **Recordset** retornado do método **OpenSchema** no objeto **Connection** não podem ser comparadas a outras variáveis. Para obter mais informações sobre os tipos de dados de banco de dados OLE, consulte o Capítulo 13 e o Apêndice A do *Microsoft OLE DB Programmer's Reference*.


