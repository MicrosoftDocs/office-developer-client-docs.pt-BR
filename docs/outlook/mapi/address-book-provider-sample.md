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
ms.openlocfilehash: c32017598407760d5dbbb01ee6c28267bbffd152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766131"
---
# <a name="address-book-provider-sample"></a>Exemplo de provedor de catálogo de endereços

  
  
**Aplica-se a**: Outlook 
  
Esta amostra oferece suporte a um único contêiner somente leitura para nomes para exibição e endereços de email, o qual serão lidas a partir de um arquivo binário plano. O exemplo suporta modelos únicos e todas as opções de configuração, exceto o Assistente de perfil.
  
Você pode baixar esse exemplo de [Amostras de código do Outlook Messaging API (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740
).
  
|||
|:-----|:-----|
|Executável:  <br/> |SABP32.dll  <br/> |
| Diretório de origem do código:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos compatíveis

Este exemplo aceita os seguintes recursos:
  
- Restrições de tabela. O exemplo implementa a resolução de nome ambígua e de correspondência de prefixo. Ele não implementa o idioma de restrição de MAPI completo e restrições são compatíveis apenas com o nome para exibição.
    
- Uma tabela de exibição de detalhes para os usuários de mensagens. 
    
- Endereços únicos.
    
- Uma caixa de diálogo de pesquisa avançada.
    
- Um [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface. Esta interface é suportada parcialmente; seus métodos **IMAPIProp** delegados para a interface **IPropData** . Para obter mais informações, consulte o [IPropData: IMAPIProp](ipropdataimapiprop.md) interface. 
    
- Configuração interativa e programática.
    
## <a name="unsupported-features"></a>Recursos sem suporte

Este exemplo não suporta os seguintes recursos:
  
- Classificando.
    
- Listas de distribuição.
    
- Criar, excluir e modificar entradas.
    
- Propriedades com vários valores.
    
- Propriedades nomeadas.
    
- Fazer a distinção entre os nomes e o sobrenome em nomes de exibição.
    
 **Para instalar o provedor de catálogo de endereços de amostra**
  
1. Para baixar o provedor de catálogo de endereços de amostra, consulte [Baixando as amostras de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Localize a pasta onde você salvou as amostras de MAPI do Outlook. Com o botão direito do **OutlookMAPISamples -\<o número de versão\> ** zip pasta e clique em **Extrair tudo**.
    
3. Clique em **Procurar**, selecione o local onde deseja salvar a amostra e clique em **extrair**.
    
4. Execute o Visual Studio 2008.
    
5. No Visual Studio 2008, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.
    
6. Navegue até o local onde você salvou a amostra, clique em **SABP.vcproj**e, em seguida, clique em **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.
    
9. Na pasta onde você salvou a amostra, com o botão direito do arquivo **Install. bat** e clique em **Executar como administrador**.
    
10. Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.
    
    > [!NOTE]
    > **Install. bat** copia o arquivo. dll na pasta de instalação do Microsoft Office padrão, C:\Program Files\Microsoft Office\Office12\. Se você tiver instalado os produtos do Office em um local diferente, clique com o botão **Install. bat** e clique em **Editar**. O arquivo será aberto no bloco de notas. Substitua o caminho de instalação padrão do caminho de instalação usado no seu computador. 
  

