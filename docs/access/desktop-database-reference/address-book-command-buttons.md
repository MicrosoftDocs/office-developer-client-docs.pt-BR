---
title: Botões de comando do Catálogo de Endereços
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282475"
---
# <a name="address-book-command-buttons"></a>Botões de comando do Catálogo de Endereços


**Aplica-se ao:** Access 2013, Office 2013


O aplicativo de Catálogo de endereços inclui os seguintes botões de comando:

- Um botão **Localizar** para enviar uma consulta ao banco de dados.

- Um botão **Desmarcar** para desmarcar as caixas de texto antes de iniciar uma nova pesquisa.

- Um botão **Atualizar perfil** para salvar as alterações em um registro de funcionário.

- Um botão **Cancelar alterações** para descartar as alterações.

## <a name="find-button"></a>Botão Localizar

Clicar no botão **Localizar** ativa o procedimento de função\_do VBScript Find OnClick, que cria e envia a consulta SQL. Clicar nesse botão preenche a grade de dados.

## <a name="building-the-sql-query"></a>Criando a consulta SQL

A primeira parte do procedimento de\_função find OnClick cria a consulta SQL, uma frase por vez, acrescentando cadeias de caracteres de texto a uma instrução SQL SELECT global. Ele começa definindo a variável como uma instrução SQL SELECT que solicita todas as linhas de dados da tabela de fonte de dados. Em seguida, o procedimento Sub analisa cada uma das quatro caixas de entrada na página.

Como o programa usa a palavra para compilar as instruções SQL, as consultas são subcadeias de caracteres em vez de correspondências exatas.

Por exemplo, se a caixa **último nome** continha a entrada "Berge" e a caixa **título** continha a entrada "gerente de programas", a instrução SQL (valor) seria a leitura:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Se a consulta foi bem-sucedida, todas as pessoas com o último nome contendo o texto "Berge" (como Berge e Berger) e com um cargo contendo as palavras "Program Manager" (por exemplo, Program Manager, Advanced Technologies) serão exibidas na grade de dados HTML.

## <a name="preparing-and-sending-the-query"></a>Preparando e enviando a consulta

A última parte do procedimento de\_função find OnClick consiste em duas instruções. A primeira atribui a propriedade SQL do objeto RDS.DataControl à consulta SQL criada de forma dinâmica. A segunda instrução faz com que o **RDS. **Objeto DataControl () para consultar o banco de dados e, em seguida, exiba os novos resultados da consulta na grade.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Botão Atualizar perfil

Clicar no botão **Atualizar perfil** ativa o procedimento da função\_do VBScript Update OnClick, que executa o RDS. Métodos SubmitChanges e Refresh do objeto dataControl.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Quando DC1. O SubmitChanges é executado, o serviço de dados remoto empacota todas as informações de atualização e as envia ao servidor via HTTP. A atualização ocorre em tudo ou em nada; se uma parte da atualização não tiver sucesso, nenhuma das alterações será feita, e uma mensagem de status será retornada. é executado, o Serviço de dados remoto cria pacote de todas as informações de atualização e os envia ao servidor via HTTP. A atualização ocorre em tudo ou em nada; se uma parte da atualização não tiver sucesso, nenhuma das alterações será feita, e uma mensagem de status será retornada. DC1. A atualização não é necessária após o **SubmitChanges** com o Remote Data Service, mas garante dados atualizados.

## <a name="cancel-changes-button"></a>Botão Cancelar alterações

Clicar em **cancelar alterações** ativa o procedimento do\_VBScript Cancel OnClick sub, que executa o RDS. Objeto dataControl (método CancelUpdate.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Quando é executado, ele descarta todas as edições feitas por um usuário em um registro de funcionário na grade de dados desde a última consulta ou atualização. Ele restaura os valores originais.

