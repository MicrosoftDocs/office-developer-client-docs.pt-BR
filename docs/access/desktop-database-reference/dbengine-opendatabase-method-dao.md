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
ms.openlocfilehash: 54078705c67e892b80a08ce2bd31db191c7fc70c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606154"
---
# <a name="dbengineopendatabase-method-dao"></a>Método DBEngine.OpenDatabase (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Abre um banco de dados especificado e retorna uma referência ao objeto **[Database](database-object-dao.md)** que o representa.

## <a name="syntax"></a>Sintaxe

*expressão* . OpenDatabase (***nome***, ***Opções***, ***ReadOnly***, ***Conecte-se***)

*expressão* Uma variável que representa um objeto **DBEngine** .

### <a name="parameters"></a>Parâmetros

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
<td><p>Name</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>o nome de um arquivo de banco de dados existente do Microsoft Access ou o DSN (nome da fonte de dados) de uma fonte de dados ODBC. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter mais informações sobre como configurar esse valor.</p></td>
</tr>
<tr class="even">
<td><p>Opções</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Define as várias opções para o banco de dados, como especificado em Comentários.</p></td>
</tr>
<tr class="odd">
<td><p>ReadOnly</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> se você quiser abrir o banco de dados com acesso somente leitura, ou <strong>False</strong> (padrão) se você quiser abrir o banco de dados com acesso de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p>Connect</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica várias informações de conexão, incluindo senhas.</p></td>
</tr>
</tbody>
</table>


<<<<<<< Cabeça
### <a name="return-value"></a>Valor retornado
=======
### <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

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

Para fechar um banco de dados e assim remover o objeto **Database** da coleção **Databases**, use o método **[Close](connection-close-method-dao.md)** no objeto.


> [!NOTE]
> <P>[!OBSERVAçãO] Ao acessar uma fonte de dados ODBC conectada a um mecanismo de banco de dados do Microsoft Access, você pode aprimorar o desempenho do seu aplicativo abrindo um objeto <STRONG>Database</STRONG> conectado à fonte de dados ODBC, em vez de vincular objetos <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> individuais a tabelas específicas na fonte de dados ODBC.</P>


