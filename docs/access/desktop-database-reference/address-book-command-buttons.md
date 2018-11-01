---
title: Botões de comando do Catálogo de endereços
TOCTitle: Address Book Command Buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e445414ead78bb5e1b05b3f3812e86f1d6c119ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869509"
---
# <a name="address-book-command-buttons"></a>Botões de comando do Catálogo de endereços


**Aplica-se a**: Access 2013, o Office 2013


O aplicativo de Catálogo de endereços inclui os seguintes botões de comando:

  - Um botão Localizar para enviar uma consulta ao banco de dados.

  - Um botão **Desmarcar** para desmarcar as caixas de texto antes de iniciar uma nova pesquisa.

  - Um botão Atualizar perfil para salvar as alterações em um registro de funcionário.

  - Um botão Cancelar alterações para descartar as alterações.

## <a name="find-button"></a>Botão Localizar

Clicar no botão **Localizar** ativa o VBScript localizar\_procedimento Sub de OnClick, que cria e envia a consulta SQL. Clicar nesse botão preenche a grade de dados.

## <a name="building-the-sql-query"></a>Criando a consulta SQL

A primeira parte do localizar\_procedimento OnClick Sub cria a consulta SQL, uma frase de cada vez, acrescentando cadeias de caracteres de texto para uma instrução de SQL SELECT global. Ele começa definindo-se a variável como uma instrução SQL que as solicitações de todas as linhas de dados da tabela da fonte de dados. Em seguida, o procedimento Sub analisa cada uma das quatro caixas de entrada na página.

Como o programa usa a palavra na criação das instruções SQL, as consultas são pesquisas de subcadeia de caracteres em vez de correspondências exatas.

Por exemplo, se a caixa **Último nome** continha a entrada "Berge" e a caixa **cargo** continha a entrada "Program Manager", a instrução SQL (valor) leria:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Se a consulta foi bem-sucedida, todas as pessoas com o último nome contendo o texto "Berge" (como Berge e Berger) e com um cargo contendo as palavras "Program Manager" (por exemplo, Program Manager, Advanced Technologies) serão exibidas na grade de dados HTML.

## <a name="preparing-and-sending-the-query"></a>Preparando e enviando a consulta

A última parte da localizar\_procedimento OnClick Sub consiste em duas instruções. A primeira atribui a propriedade SQL do objeto RDS.DataControl à consulta SQL criada de forma dinâmica. A segunda instrução faz com que o **RDS. DataControl** () para consultar o banco de dados de objeto e, em seguida, exiba os novos resultados da consulta na grade.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Botão Atualizar perfil

Clicar no botão **Atualizar perfil** ativa a atualização do VBScript\_procedimento OnClick Sub, que executa o RDS. () SubmitChanges e Refresh métodos do objeto DataControl.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Quando DC1. Executa SubmitChanges, o serviço de dados remotos todas as informações de atualização de pacotes e enviá-la para o servidor via HTTP. A atualização ocorre em tudo ou em nada; se uma parte da atualização não tiver sucesso, nenhuma das alterações será feita, e uma mensagem de status será retornada. é executado, o Serviço de dados remoto cria pacote de todas as informações de atualização e os envia ao servidor via HTTP. A atualização ocorre em tudo ou em nada; se uma parte da atualização não tiver sucesso, nenhuma das alterações será feita, e uma mensagem de status será retornada. DC1. A atualização não é necessária depois de **SubmitChanges** com o Remote Data Service, mas garante dados atualizados.

## <a name="cancel-changes-button"></a>Botão Cancelar alterações

Clicar em **Cancelar alterações** ativa o cancelamento do VBScript\_procedimento OnClick Sub, que executa o RDS. Do objeto DataControl (método CancelUpdate.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Quando é executado, ele descarta todas as edições feitas por um usuário para um registro de funcionário na grade de dados desde a última consulta ou atualização. Ele restaura os valores originais.

