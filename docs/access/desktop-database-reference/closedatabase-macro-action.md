---
title: Ação da macro FecharBancoDeDados
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d55e2028027f0861b1e9ad00518d9c51180fdfc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919877"
---
# <a name="closedatabase-macro-action"></a>Ação da macro FecharBancoDeDados


**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **FecharBancoDeDados** para fechar o banco de dados atual.

## <a name="setting"></a>Configuração

A ação **FecharBancoDeDados** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

  - O Access não executará nenhuma ação que siga a ação **FecharBancoDeDados** em uma macro.

  - Essa ação tem o mesmo efeito que clicar na guia **arquivo** e clicando em **Fechar do banco de dados**. Se houver algum objeto não salvo ao executar a ação **FecharBancoDeDados**, as caixas de diálogo exibidas serão as mesmas daquelas exibidas ao clicar em **Fechar Banco de Dados**.

  - Para executar a ação **FecharBancoDeDados** em um módulo do VBA (Visual Basic for Applications), use o método **CloseDatabase** do objeto **DoCmd**.

