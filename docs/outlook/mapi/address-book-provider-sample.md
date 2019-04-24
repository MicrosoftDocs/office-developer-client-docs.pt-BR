---
title: Exemplo de provedor de catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331105"
---
# <a name="address-book-provider-sample"></a>Exemplo de provedor de catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este exemplo suporta um único contêiner somente leitura para nomes de exibição e endereços de email, que são lidos de um arquivo binário simples. O exemplo suporta modelos one-off e todas as opções de configuração, exceto o assistente de perfil.
  
Você pode baixar esse exemplo de [exemplos de código da API de mensagens do Outlook (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740
).
  
|||
|:-----|:-----|
|Arquivo  <br/> |SABP32. dll  <br/> |
| Diretório do código-fonte:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Pacote  <br/> |C++  <br/> |
|Plataformas  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos com suporte

Este exemplo oferece suporte aos seguintes recursos:
  
- Restrições de tabela. O exemplo implementa a correspondência de prefixo e de nomes ambíguos. Ele não implementa o idioma de restrição de MAPI completo e só há suporte para restrições no nome de exibição.
    
- Uma tabela de exibição de detalhes para usuários de mensagens. 
    
- Endereços únicos.
    
- Uma caixa de diálogo de pesquisa avançada.
    
- Uma interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Essa interface é parcialmente suportada; seus métodos **IMAPIProp** são delegados para a interface **IPropData** . Para obter mais informações, consulte a interface [IPropData: IMAPIProp](ipropdataimapiprop.md) . 
    
- Configuração interativa e programática.
    
## <a name="unsupported-features"></a>Recursos sem suporte

Este exemplo não é compatível com os seguintes recursos:
  
- Sorting.
    
- Listas de distribuição.
    
- Criar, excluir e modificar entradas.
    
- Propriedades com vários valores.
    
- Propriedades nomeadas.
    
- Distinguir entre nome e sobrenome em nomes de exibição.
    
 **Para instalar o provedor de catálogo de endereços de exemplo**
  
1. Para baixar o provedor de catálogo de endereços de exemplo, confira [download dos exemplos de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Localize a pasta onde você salvou os exemplos de MAPI do Outlook. Clique com o botão direito do mouse na pasta zip **OutlookMAPISamples número\<\> de versão** e clique em **extrair tudo**.
    
3. Clique em **procurar**, selecione o local onde deseja salvar o exemplo e clique em **extrair**.
    
4. Execute o Visual Studio 2008.
    
5. No Visual Studio 2008, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.
    
6. Navegue até o local onde você salvou o exemplo, clique em **SABP. vcproj**e, em seguida, clique em **abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.
    
9. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install. bat** e clique em **Executar como administrador**.
    
10. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
    > [!NOTE]
    > **Install. bat** copia o. dll para a pasta de instalação padrão do Microsoft Office, C:\Arquivos de Programas\Microsoft Office\OFFICE12\. Se você tiver instalado os produtos do Office em um local diferente, clique com o botão direito em **instalar. bat** e clique em **Editar**. O arquivo é aberto no bloco de notas. Substitua o caminho de instalação padrão pelo caminho de instalação usado no computador. 
  

