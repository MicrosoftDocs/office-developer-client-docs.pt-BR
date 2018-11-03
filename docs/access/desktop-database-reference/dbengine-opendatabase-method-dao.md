---
title: Método DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eb3f6795ba2e64ebd6be1b04d6aa6aecccef781b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950087"
---
# <a name="dbengineopendatabase-method-dao"></a>Método DBEngine.OpenDatabase (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Abre um banco de dados especificado e retorna uma referência ao objeto **[Database](database-object-dao.md)** que o representa.

## <a name="syntax"></a>Sintaxe

*expressão* . OpenDatabase (***nome***, ***Opções***, ***ReadOnly***, ***Conecte-se***)

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Nome</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>o nome de um arquivo de banco de dados existente do Microsoft Access ou o DSN (nome da fonte de dados) de uma fonte de dados ODBC. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter mais informações sobre como configurar esse valor.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Define as várias opções para o banco de dados, como especificado em Comentários.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> se você quiser abrir o banco de dados com acesso somente leitura, ou <strong>False</strong> (padrão) se você quiser abrir o banco de dados com acesso de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica várias informações de conexão, incluindo senhas.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Banco de dados

## <a name="remarks"></a>Comentários

Você pode usar os valores a seguir para o argumento options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuração</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Abre o banco de dados no modo exclusivo.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(Padrão) Abre o banco de dados no modo compartilhado.</p></td>
</tr>
</tbody>
</table>


Quando você abre um banco de dados, ele é automaticamente adicionado à coleção **Databases**.

Algumas considerações se aplicam quando se usa dbname:

- Se ela se referir a um banco de dados que já foi aberto para acesso por outro usuário, ocorrerá um erro.

- Se ela não se referir a um banco de dados existente ou validar o nome da fonte de dados ODBC, ocorrerá um erro.

- Se for uma cadeia de caracteres de comprimento zero ("") e *Conecte-se* for "ODBC;", uma caixa de diálogo listando todos os registrados nomes de fonte de dados ODBC é exibida para que o usuário possa selecionar um banco de dados.

Para fechar um banco de dados e, desse modo, remover o objeto **Database** da coleção **Databases**, use o método **[Close](connection-close-method-dao.md)** no objeto.

> [!NOTE]
> [!OBSERVAçãO] Ao acessar uma fonte de dados ODBC conectada a um mecanismo de banco de dados do Microsoft Access, você pode aprimorar o desempenho do seu aplicativo abrindo um objeto **Database** conectado à fonte de dados ODBC, em vez de vincular objetos [TableDef](tabledef-object-dao.md) individuais a tabelas específicas na fonte de dados ODBC.


