FROM archlinux
ENV RUN_MODE=serve

RUN pacman -Syu --noconfirm
RUN pacman -Sy --noconfirm ruby base-devel ruby-erb
RUN pacman -Sy --noconfirm wget
RUN gem install bundler jekyll jekyll-sitemap

WORKDIR /root

RUN echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
RUN echo 'export GEM_HOME='$(ruby -e 'puts Gem.user_dir')'' >> ~/.bashrc
RUN echo 'export PATH="$PATH:$GEM_HOME/bin"' >> ~/.bashrc
RUN source ~/.bashrc


EXPOSE 4000
CMD source ~/.bashrc && bash -c 'echo DDD'