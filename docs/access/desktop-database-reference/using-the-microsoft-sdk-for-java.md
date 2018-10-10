---
title: Usando o Microsoft SDK for Java
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbcae50b0fdecc441bab40894899a75d04ee5f72
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461994"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Usando o Microsoft SDK for Java


**Aplica-se a**: Access 2013 | Office 2013

O Microsoft SDK for Java é o kit de desenvolvedor para o ambiente Microsoft Internet Explorer. Ferramentas, informações e exemplos são fornecidos para ajudá-lo a desenvolver programas e miniaplicativos Java baseados no JDK 1.1 e no Microsoft Win32 virtual machine (Microsoft VM). O Microsoft SDK for Java não está restrito ao Microsoft Visual J++.

O utilitário Jactivex.exe gera classes de uma biblioteca de tipos, mas somente pode ser chamado na linha de comando. Esse recurso não está integrado ao ambiente de desenvolvimento do Visual J++. Ao contrário das classes geradas pelo [Java Type Library Wizard](using-the-java-type-library-wizard.md), você pode entrar nos invólucros de classe criados pelo SDK, o que é útil para depurar o modo de uso das classes invólucro ADO pelo seu código.

Esse mecanismo lê a biblioteca de tipos ADO e gera classes que podem ser instanciadas em seu aplicativo. Ele gera esses classes no seguinte local: \\ \<diretório windows\>\\Java\\trustlib\\msado15.

A criação de um aplicativo ADO em Java com o Microsoft SDK for Java é basicamente idêntico, da perspectiva do código-fonte, ao uso do Java Type Library Wizard. Para obter um código de exemplo, consulte [Invólucros de classe ADO Java](ado-java-class-wrappers.md). A única diferença real está no modo como você gera as classes invólucro em primeiro lugar, conforme demonstrado nas etapas a seguir.

**Para criar um projeto ADO com o Microsoft SDK for Java**

1.  Execute o seguinte em um prompt de comando. Defina o caminho para incluir o diretório Bin do Microsoft SDK for Java, ou execute o comando a partir desse local. Em geral, o Microsoft SDK for Java está instalado no mesmo local do Visual Studio. Esta é uma instrução de comando único.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Execute o comando a seguir para compilar as classes geradas. A opção /g:t ativa a geração de símbolos de depuração, para que você possa rastrear nos símbolos .Java. Remova-a para as compilações de versão.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Para usar esses arquivos, abra seu projeto no Visual J++. No menu **Projeto**, escolha **Adicionar ao Projeto**. Selecione os **arquivos**e adicione todos os. Arquivos JAVA gerados no trustlib\\msado15 directory ao seu projeto.
