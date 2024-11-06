FROM multi2sim/multi2sim:latest

# Set non-interactive mode
ENV DEBIAN_FRONTEND=noninteractive

# Update and install zsh and other necessary packages
RUN apt update -y && \
    apt install -y zsh git curl

# Change default shell to zsh
RUN chsh -s $(which zsh)

# Enable zsh history
RUN touch /root/.zsh_history && \
    echo "HISTFILE=/root/.zsh_history" >> ~/.zshrc && \
    echo "HISTSIZE=1000" >> ~/.zshrc && \
    echo "SAVEHIST=1000" >> ~/.zshrc && \
    echo "setopt INC_APPEND_HISTORY" >> ~/.zshrc && \
    echo "setopt SHARE_HISTORY" >> ~/.zshrc

# Install zsh plugins
RUN git clone --depth=1 https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
RUN echo "source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc

RUN git clone --depth=1 https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting
RUN echo "source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc

# RUN git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.zsh/powerlevel10k
# RUN echo "source ~/.zsh/powerlevel10k/powerlevel10k.zsh-theme" >>~/.zshrc

RUN echo "PROMPT='%~ > '" >> ~/.zshrc

CMD [ "zsh" ]