cmake_minimum_required(VERSION 3.19)
project(DerClou VERSION 2.7
  DESCRIPTION "Der Clou! - SDL Port"
  HOMEPAGE_URL "https://github.com/NewProggie/derclou"
  LANGUAGES C)

find_package(SDL2 REQUIRED)

add_executable(DerClou
  anim/sysanim.c
  base/base.c
  cdrom/cdrom.c
  data/dataappl.c
  data/database.c
  data/datacalc.c
  data/relation.c
  dialog/dialog.c
  dialog/talkappl.c
  disk/disk.c
  error/error.c
  gameplay/gp_app.c
  gameplay/gp.c
  gameplay/loadsave.c
  gameplay/tcreques.c
  gfx/gfx.c
  gfx/gfxnch4.c
  inphdl/inphdl.c
  landscap/access.c
  landscap/landscap.c
  landscap/hardware.c
  landscap/init.c
  landscap/raster.c
  landscap/scroll.c
  landscap/spot.c
  list/list.c
  living/bob.c
  living/living.c
  memory/memory.c
  organisa/organisa.c
  planing/graphics.c
  planing/guards.c
  planing/io.c
  planing/main.c
  planing/planer.c
  planing/player.c
  planing/prepare.c
  planing/support.c
  planing/system.c
  planing/sync.c
  present/present.c
  present/interac.c
  random/random.c
  scenes/cars.c
  scenes/dealer.c
  scenes/done.c
  scenes/evidence.c
  scenes/inside.c
  scenes/invest.c
  scenes/scenes.c
  scenes/tools.c
  sound/buffer.c
  sound/fmopl.c
  sound/fx.c
  sound/newsound.c
  sound/hsc.c
  story/story.c
  text/text.c)

set_target_properties(DerClou
  PROPERTIES C_STANDARD 90)

target_link_libraries(DerClou SDL2::SDL2 m)

target_include_directories(DerClou
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})

target_compile_options(DerClou
  PRIVATE -pedantic -Wall -Wmissing-prototypes -Wmissing-declarations -Wsign-compare)

target_link_options(DerClou
  PRIVATE -O2 -funroll-loops)
