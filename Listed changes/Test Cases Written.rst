#######################
Test Cases Written
#######################

.. <https://gitlab.com/OpenMW/openmw/-/issues/>`_

-------------------------------------------------------------

   `Bug #4021: <https://gitlab.com/OpenMW/openmw/-/issues/4021>`_ **Attributes and skills are not stored as floats**

      Attributes and skills now accept float values ie 0.1, 0.2, 0.135238 etc. unsure if vanilla behaviour always rounding up is replicated.

          Test: (tested by:                      )
              You can use script functions in script or console to check what happens.

-------------------------------------------------------------

   `Bug #4055: <https://gitlab.com/OpenMW/openmw/-/issues/4055>`_ **Local scripts don't inherit variables from their base record**

      it should now be possible to spawn object that inherits variables from base record.

          Test: (tested by:                      )
              make scripted changes to unique base record and observe the changes in duplicate ?

    seealso::
            feature `2798: Mutable ESM records <https://gitlab.com/OpenMW/openmw/-/issues/2798>`_ and


-------------------------------------------------------------

   `Bug #4623: <https://gitlab.com/OpenMW/openmw/-/issues/4623>`_ **Corprus implementation is incorrect**



          Test: (tested by:                      )

-------------------------------------------------------------

   `Bug #4764: <https://gitlab.com/OpenMW/openmw/-/issues/4764>`_ **Data race in osg ParticleSystem**



          Test: (tested by:                      )

-------------------------------------------------------------

  `Bug #4774: <https://gitlab.com/OpenMW/openmw/-/issues/4774>`_ **Guards are ignorant of an invisible player that tries to attack them**

      Guards now do LOS check and doesn't witch during AI pursue

          Test: (tested by:                      )
              Try to attack guards while invisible or with chameleon effect higher than 80% ?

    seealso ::
            | bugs `4920: Combat AI uses incorrect invisibility check <https://gitlab.com/OpenMW/openmw/-/issues/4920>`_
            | and `5575: Guards don't pursue the player if they don't have direct line of sight <https://gitlab.com/OpenMW/openmw/-/issues/5575>`_
            |
            | related pulls are
            | `2988: AIPursue: don't do a LOS check <https://github.com/OpenMW/openmw/pull/2988>`_
            | `2351: AI: use a consistent check if a target is hidden <https://github.com/OpenMW/openmw/pull/2351>`_

-------------------------------------------------------------

  `Bug #5108: <https://gitlab.com/OpenMW/openmw/-/issues/5108>`_ **Savegame bloating due to inefficient fog textures format**

      Fog of war storing texture was changed to PNG from TGA due to savefile size concerns

          Test: (tested by:                      )
              No really righforward way to test than
              comparing two wide area? play sessions together in 0.46 and 0.47

-------------------------------------------------------------

  `Bug #5165: <https://gitlab.com/OpenMW/openmw/-/issues/5165>`_ **Active spells should use real time instead of timestamps**

      Active spells duration will act based on real time instead of the time used in game ie. resting and timescale.
      Old saves from 0.46 will have their spell durations refreshed to max due to code simplicity.

          Test: (tested by:                      )
              If you cast let say, fireshield onto yourself it now lasts said seconds in real time.

-------------------------------------------------------------

  `Bug #5363: <https://gitlab.com/OpenMW/openmw/-/issues/5363>`_ **Enchantment autocalc not always 0/1**

      Enchantments "auto calc" field now treats values other than 0 or 1 as invalid.

          Test: (tested by:                      )
              Needs corrupted auto calc field value

-------------------------------------------------------------



***********************
AI
***********************

***********************
Combat
***********************

***********************
Controllers
***********************

***********************
Editor
***********************

***********************
Enchanting
***********************

***********************
General
***********************

***********************
Launcher
***********************

***********************
Magic
***********************

***********************
Menus
***********************

***********************
Models
***********************

  `Bug #1952: <https://gitlab.com/OpenMW/openmw/-/issues/1952>`_ `Incorrect particle lighting`

      Before of this, particles could only use their own light source,
      but now they have correct normals and look as they should
      reacting to diffuse lightning (actual light sources)

          Test: (tested by:                      )
              look upon `these candles <https://gitlab.com/OpenMW/openmw/issues/4029>`_ ,
              they shouldn’t disappear anymore or
              see Akulakhan's Chamber’s flame above akulakhan in all its glory.

-------------------------------------------------------------

  `Bug #3676: <https://gitlab.com/OpenMW/openmw/-/issues/3676>`_ `NiParticleColorModifier isn't applied properly`

      NiParticleColorModifier is now primary source for color
      and transparency ie. particle lighting system doesn’t override it anymore.

          Test: (tested by:                      )
              try the place mentioned in issue or use console to
              placeatpc steam_bluegreen 1 1 1


***********************
Saves
***********************

***********************
Scripting
***********************

  `Bug #5358: <https://gitlab.com/OpenMW/openmw/-/issues/5358>`_ `ForceGreeting always resets the dialogue window completely`

      There can now be three way conversations like in vanilla as in
      dialogue window isn’t switched when using actorid->ForceGreeting
      When the dialogue window is closed, history is cleared as in vanilla thought.

          Test: (tested by:                      )
              write a mod for the situation (?)


***********************
Stealth
***********************

***********************
Werewolf
***********************
